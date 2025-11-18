
---

> [!INFO] Teilnahmen
> Bisher wurden `$=dv.pages("#Session").where(p => !p.file.folder.startsWith("3-DM/Bibliothek/Templates")).length` Sessions gespielt mit folgenden Anwesenheiten:
---
```dataview
TABLE length(rows) as "Anzahl Teilnahmen"
FROM #Session AND !"3-DM"
FLATTEN Players as Charakter
WHERE Charakter != null
GROUP BY Charakter
SORT length(rows) DESC
```
---
```dataviewjs
// 1. Ein Objekt, um die Zählungen zu speichern
const playerCounts = new Map();

// 2. Finde alle relevanten Sessions
const sessions = dv.pages('#Session AND !"3-DM"');

// 3. Gehe jede Session einzeln durch
for (const session of sessions) {
    // 4. Ein Set, um Spieler pro Session zu de-duplizieren
    //    (verhindert doppelte Zählung bei mehreren Charakteren)
    const uniquePlayersInSession = new Set();

    // 5. Sammle alle Charaktere (Spieler + DM)
    const playerChars = session.Players ? dv.array(session.Players) : [];
    const dmChars = session.DM ? dv.array(session.DM) : [];
    const allChars = playerChars.concat(dmChars);

    // 6. Finde den "Spieler" für jeden Charakter
    for (const charLink of allChars) {
        if (!charLink) continue; // Überspringe leere Einträge
        
        const charPage = dv.page(charLink.path);
        if (!charPage) continue; // Überspringe, falls Charakter-Seite nicht existiert

        // Nimm den Spieler-Link ODER (als Fallback) den Charakter-Link selbst
        const finalEntity = charPage.Spieler || charLink;
        
        // Füge den Link zum Set hinzu. 
        // Wenn ein Spieler 2 Charaktere hat, wird er hier nur 1x gespeichert.
        uniquePlayersInSession.add(finalEntity.path);
    }

    // 7. Erhöhe die Zählung für jeden einzigartigen Spieler dieser Session
    for (const playerPath of uniquePlayersInSession) {
        const currentCount = playerCounts.get(playerPath) || 0;
        playerCounts.set(playerPath, currentCount + 1);
    }
}

// 8. Konvertiere die Map in ein sortiertes Array für die Tabelle
const sortedCounts = Array.from(playerCounts.entries())
    .map(([path, count]) => {
        // Erstelle einen klickbaren Link aus dem Pfad
        return [dv.fileLink(path), count];
    })
    .sort((a, b) => b[1] - a[1]); // Sortiere nach Anzahl (absteigend)

// 9. Zeige die finale Tabelle an
dv.table(["Spieler", "Anzahl Teilnahmen"], sortedCounts);
```
---
