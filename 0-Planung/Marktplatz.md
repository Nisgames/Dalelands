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
