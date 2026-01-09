> [!warning] 🚨 AKTUELLE Ereignisse
> ```dataviewjs
> // Suche alle aktiven Plots
> let pages = dv.pages('#Plot');
> 
> // Gehe durch alle Plots
> for (let page of pages) {
>     // Prüfe alle Listenpunkte in der Plot-Datei
>     if (page.file.lists) {
>         for (let item of page.file.lists) {
>             // Wenn der Listenpunkt auf DIESE Datei verlinkt
>             if (item.outlinks.some(l => l.path == dv.current().file.path)) {
>                 
>                 // 1. Überschrift anzeigen (welcher Plot ist das?)
>                 dv.header(4, "⚡ Aus Plot: " + page.file.name);
>                 
>                 // 2. Den Link entfernen (damit es schöner aussieht) und Text rendern
>                 // Wir entfernen "[[Dateiname]]" aus dem Text
>                 let cleanText = item.text.replace(/\[\[.*?\]\]:?/, "").trim();
>                 
>                 // 3. Den Text (inkl. Callouts!) rendern
>                 dv.paragraph(cleanText);
>             }
>         }
>     }
> }
> ```

---

```dataviewjs

// 🚨 AKTUELLE EREIGNISSE
let pages = dv.pages('#Plot'); // Sucht nach Tag #Plot

// Gehe durch alle Plots
for (let page of pages) {
    if (page.file.lists) {
        for (let item of page.file.lists) {
            // Prüfen, ob der Link auf DIESE Datei zeigt
            if (item.outlinks.some(l => l.path == dv.current().file.path)) {
                
                // Überschrift mit Link zur Plot-Datei
                dv.header(4, "⚡ Aus Plot: " + page.file.link);
                
                // TRICK: Wir laden den echten Datei-Inhalt, um auch Callouts zu erwischen
                let content = await dv.io.load(page.file.path);
                let lines = content.split("\n");
                
                // Wir holen uns alles von der Startzeile bis zum Ende des Blocks
                let start = item.position.start.line;
                let end = item.position.end.line;
                let textBlock = lines.slice(start, end).join("\n");
                
                // Den Link aus der ersten Zeile entfernen (Optik)
                // Entfernt "[[Dateiname]]:" am Anfang
                textBlock = textBlock.replace(/-\s*\[\[.*?\]\]:?/, "").trim();
                
                // Rendern
                dv.paragraph(textBlock);
            }
        }
    }
}

```


---


```dataviewjs
// --- DEBUG START ---
dv.header(3, "🕵️ Debug Protokoll");

// 1. Suche nach Dateien mit Tag #Plot
let pages = dv.pages('#Plot');
dv.paragraph("🔍 **Suche Tag #Plot:** Habe " + pages.length + " Dateien gefunden.");

if (pages.length == 0) {
    dv.paragraph("❌ **Fehler:** Keine Dateien mit `#Plot` gefunden! Überprüfe, ob deine Plot-Datei wirklich diesen Tag hat.");
} else {
    // 2. Gehe durch die Dateien
    for (let page of pages) {
        dv.paragraph("📂 **Prüfe Datei:** " + page.file.name);
        
        if (page.file.lists.length == 0) {
            dv.paragraph("   -> ⚠️ Datei hat keine Bulletpoints (Listenpunkte).");
        }
        
        for (let item of page.file.lists) {
            // 3. Prüfe Links
            if (item.outlinks.length > 0) {
                let link = item.outlinks[0];
                dv.paragraph("   -> 🔗 Link gefunden zu: `" + link.path + "`");
                
                // 4. Vergleich mit aktueller Datei
                let currentPath = dv.current().file.path;
                dv.paragraph("      -> Vergleich mit: `" + currentPath + "`");
                
                if (link.path == currentPath) {
                    dv.paragraph("      -> ✅ **TREFFER!** Pfad stimmt exakt überein.");
                } else {
                    dv.paragraph("      -> ❌ Pfad stimmt NICHT überein.");
                }
            }
        }
    }
}
// --- DEBUG ENDE ---
```


```dataviewjs
// 🚨 AKTUELLE EREIGNISSE (Tolerante Version)
// 1. Hole alle Dateien mit Tag #Plot
let pages = dv.pages('#Plot');

for (let page of pages) {
    if (page.file.lists) {
        for (let item of page.file.lists) {
            // 2. PRÜFUNG: Zeigt einer der Links auf MICH?
            // Wir prüfen, ob der Pfad des Links meinen Dateinamen enthält
            let isMatch = item.outlinks.some(l => l.path === dv.current().file.path);
            
            if (isMatch) {
                // Überschrift
                dv.header(4, "⚡ Aus Plot: " + page.file.link);
                
                // Inhalt laden und säubern
                let content = await dv.io.load(page.file.path);
                let lines = content.split("\n");
                let start = item.position.start.line;
                let end = item.position.end.line;
                let textBlock = lines.slice(start, end).join("\n");
                
                // Entfernt den Link "[[...]]" aus der Anzeige für schönere Optik
                textBlock = textBlock.replace(/-\s*\[\[.*?\]\]:?/, "").trim();
                
                dv.paragraph(textBlock);
            }
        }
    }
}
```
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
                
                // Entfernt den Link "- [[Ort]]:" am Anfang für saubere Optik
                textBlock = textBlock.replace(/-\s*\[\[.*?\]\]:?/, "").trim();
                
                // 5. Anzeigen
                dv.paragraph(textBlock);
            }
        }
    }
}

if (!foundAny) {
    dv.paragraph("_Keine aktiven Events für diesen Ort._");
}
```
