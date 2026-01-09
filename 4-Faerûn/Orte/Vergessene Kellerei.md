---
tags:
  - Ort
Liegt_in: "[[Cormanthor]]"
Fraktionen: "[[Haus Jaelre]]"
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
-

## Aufbau

- Ein überwucherter Kellerzugang aus grauem Stein, verborgen unter den Wurzeln einer riesigen Eiche
- Etwa eine Stunde außerhalb von [[Ashabenford]]
- Dient als Versteck für den Dieb, der den [[Schattensplitter]] gestohlen hat
- Die Architektur deutet auf die Zeit vor dem Fall von Myth Drannor hin.

> [!vorlesen] Der Abstieg
> "Die steinerne Treppe führt steil in die Dunkelheit. Die Luft hier unten ist kühl und riecht nicht nach Moder, sondern seltsam sauber."

### Raum 1: Die Vorhalle
* **Beschreibung:** Ein quadratischer Raum (6x6m), alte Weinfässer sind zerborsten. Spinnweben hängen dick von der Decke.
* **Begegnung:** 2x **[[Schatten-Spinne]]**. Sie lauern an der Decke.
    * *Flavor:* Sie sind nicht normal. Ihre Augen glühen schwach violett (Einfluss der Splitter).
* **Loot:** In einem Kokon findet sich ein alter *Trank der Heilung*.

### Raum 2: Der Riss
* **Beschreibung:** Der Gang ist eingestürzt. Ein Riss im Boden klafft auf, der etliche Meter tief zu sein scheint. Man muss springen oder klettern.
* **Hindernis:** Der Dieb hat eine Falle hinterlassen (Stolperdraht vor dem Sprung).
    * *Check:* **Perception DC 13**.
    * *Effekt:* Armbrustbolzen (**1d6 Schaden**)

### Raum 3: Die Kammer des Echos
* **Beschreibung:** Eine alte Statue einer Elfen-Gottheit, deren Gesicht zerschlagen wurde.
* **Phänomen:** Wenn die Spieler sprechen, hören sie ihre Worte erst minimal verzögert nach dem Sprechen
* **Hinweis:** Dies dient nur der Atmosphäre und zeigt die Zeit-Verzerrung.

### Raum 4: Das Ritual
* **NPC:** [[Varon]] (Drow Spion) kniet vor einem Altar.
* 
* **Gegner:** [[Varon]], der sich aus dem Altar löst.


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
