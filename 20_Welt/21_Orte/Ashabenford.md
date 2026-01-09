---
tags:
  - Ort
Liegt_in: "[[Mistledale]]"
Fraktionen:
---

```dataviewjs
// 🚨 AKTUELLE EREIGNISSE (Scanner Version)
let pages = dv.pages('#Plot');
let foundAny = false;

for (let page of pages) {
    if (page.file.lists) {
        for (let item of page.file.lists) {
            
            // 1. Prüfen: Zeigt der Link auf MICH? (Namens-Check)
            let myName = dv.current().file.name;
            let isMatch = item.outlinks.some(l => l.path.includes(myName));
            
            if (isMatch) {
                foundAny = true;
                dv.header(4, "⚡ Aus Plot: " + page.file.link);
                
                // 2. Datei-Inhalt laden
                let content = await dv.io.load(page.file.path);
                // Splitte Text in Zeilen (funktioniert für Windows & Mac)
                let lines = content.split(/\r?\n/);
                
                // 3. Manuelles Einsammeln: Start beim Bulletpoint
                let startLine = item.position.start.line;
                let capturedLines = [];
                
                // Erste Zeile (den Bulletpoint selbst) nehmen
                capturedLines.push(lines[startLine]);
                
                // Jetzt schauen wir uns die nächsten Zeilen an
                for (let i = startLine + 1; i < lines.length; i++) {
                    let line = lines[i];
                    
                    // STOPP-BEDINGUNG:
                    // Wenn eine neue Zeile mit "-" oder "*" oder "#" (Überschrift) beginnt,
                    // ist unser aktueller Punkt zu Ende.
                    if (line.match(/^[-*]\s/) || line.match(/^#+\s/)) {
                        break;
                    }
                    // Ansonsten: Zeile gehört dazu (auch Callouts!)
                    capturedLines.push(line);
                }
                
                // 4. Zusammenbauen & Säubern
                let textBlock = capturedLines.join("\n");
                
                // Entfernt den Link "- [[...]]:" am Anfang für saubere Optik
                textBlock = textBlock.replace(/-\s*\[\[.*?\]\]:?/, "").trim();
                
                // 5. Anzeigen
                dv.paragraph(textBlock);
            }
        }
    }
}

if (!foundAny) {
    dv.paragraph("_Keine aktiven Events._");
}
```
## 📖 Allgemeinwissen
Die Hauptstadt von **[[Mistledale]]**. 
Es ist ein offenes, geschäftiges Handelszentrum. 
Anders als manch andere Täler ist man hier friedlich und tolerant.

#### Glauben
In Ashabenford betet man pragmatisch:
- **Chauntea:** Für die Ernte (es ist ein Bauerntal).
- **Tymora:** Für das Glück im Handel.

#### Hoher Rat
[[Ashabenford]] wird von einem Rat regiert ([[Bürgermeisterin Andra]]). 
Sie suchen händeringend nach Söldnern, um die Straßen sicher zu halten.

## 📰 Aktuelle Gerüchte & Plot-Hooks
```dataview
TABLE WITHOUT ID 
file.link AS "Plot",
regexreplace(Rows.text, "\[\[.*?\]\]", "") AS "Was passiert hier?"
FROM #Plot 
FLATTEN file.lists AS Rows
WHERE contains(Rows.outlinks, this.file.link) AND !file.frontmatter.resolved
```

## Bewohner
```dataview
TABLE WITHOUT ID
	file.link as Name,
	Relevanz as Relevanz
from #NPC AND !"3-DM/"
where contains(Wohnort, this.file.link)
```
