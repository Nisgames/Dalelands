---
tags:
  - NPC
Wohnort: "[[Daggerdale]]"
Klasse:
Volk:
Level:
Fraktionen:
Status: Tot
Relevanz: Mittel
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
# `=this.file.name`
*Klasse/Beruf:* `=this.Klasse` 
*Volk:* `=this.Volk` 
*Wohnort:* `=this.Wohnort` 
*Aussehen:* 
*Charakterzug:* 
*Sprechweise:* 

# Aussehen



# Beziehungen
- 
