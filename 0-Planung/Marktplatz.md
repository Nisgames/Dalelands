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
