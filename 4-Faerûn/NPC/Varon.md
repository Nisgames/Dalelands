---
tags:
  - NPC
Wohnort: "[[Vergessene Kellerei]]"
Klasse:
Volk: Drow
Level:
Fraktionen:
Status: Lebendig
Relevanz: Mittel
statblock: inline
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

## 📰 Aktuelle Gerüchte & Plot-Hooks
```dataview
TABLE WITHOUT ID 
file.link AS "Plot",
regexreplace(Rows.text, "\[\[.*?\]\]", "") AS "Was passiert hier?"
FROM #Plot 
FLATTEN file.lists AS Rows
WHERE contains(Rows.outlinks, this.file.link) AND !file.frontmatter.resolved
```

```statblock
name: Varon
source: Monsterhandbuch 2014
size: Mittelgroß
type: Humanuider
subtype: Elf
alignment: Neutral Böse
ac: 18
hp: 71
hit_dice: 11d8+22
speed: 9 m
saves:
- Stärke: 1
- Geschicklichkeit: 7
- Konstitution: 5
- Intelligenz: 0
- Weisheit: 4
- Charisma: 1
skillsaves:
- Heimlichkeit: 10
- Wahrnehmung: 4
senses: Dunkelsicht 36 m, passive Wahrnehmung 14
languages: Elfisch, Gemeinsprache der Unterreiche
cr: 5
traits:
- [Feenblut, "Der Drow hat einen Vorteil bei Rettungswürfen, wenn er bezaubert werden soll, und Magie kann ihn nicht einschläfern."]
- ["Empfindlich gegenüber Sonnenlicht", "Solange sich der Drow im Sonnenlicht befindet, erledet er einen Nachteil auf Angriffswürfe, sowie auf Würfe mit Weißheit (Wahrnehmung), die auf Sicht beruhen."]
actions:
- [Mehrfachangriff, "Der Drow führt zwei Kurzschwert-Angriffe aus. Kurzschwert. Nahkampf-Waffenangriff: +7 zum Treffen, Reichweite 1,5 m, ein Ziel. Treffer 7 (1d6 + 4) Stichschaden plus 10 (3d6) Giftschaden"]
- [Handarmbrust, "Fernkampf-Waffenangriff"]
reactions:
- [Parade, "Der Drow addiert 3 auf seine RK gegen einen Nahkampfangriff, der ihn treffen würde. Dazu muss der Drow den Angreifer sehen und eine Nahkampfwaffe führen."]
```
