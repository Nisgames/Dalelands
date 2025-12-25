<%*
// 1. Ort abfragen (Pop-up)
const ortInput = await tp.system.prompt("Welcher Ort? (Leer lassen für alle)");

const targetTag = "Zufallsbegegnung"; 
// NAME DEINES TEMPLATE-ORDNERS HIER EINTRAGEN:
const templateFolder = "3-DM/Bibliothek/Templates"; 

const files = app.vault.getMarkdownFiles().filter(file => {
    // 2. Template selbst ausschließen (filtert ganzen Ordner)
    if (file.path.includes(templateFolder)) return false; 

    const cache = app.metadataCache.getFileCache(file);
    const fm = cache?.frontmatter;
    if (!fm) return false;

    // Tags sammeln & bereinigen (# entfernen)
    const frontmatterTags = fm.tags ? (Array.isArray(fm.tags) ? fm.tags : [fm.tags]) : [];
    const textTags = cache.tags ? cache.tags.map(t => t.tag) : [];
    const allTags = [...frontmatterTags, ...textTags].map(t => t.replace('#', ''));

    // Bedingungen
    const hatZufallTag = allTags.includes(targetTag);
    const istErledigt = fm.Erledigt === true || fm.erledigt === true;
    
    // 3. Orts-Filter: Prüft, ob der eingegebene Ort als Tag vorhanden ist
    let ortPasst = true;
    if (ortInput && ortInput.trim() !== "") {
        // Vergleicht kleingeschrieben, damit "ashabenford" auch "Ashabenford" findet
        ortPasst = allTags.some(t => t.toLowerCase() === ortInput.toLowerCase());
    }

    return hatZufallTag && !istErledigt && ortPasst;
});

if (files.length > 0) {
    const randomFile = files[Math.floor(Math.random() * files.length)];
    tR += `![[${randomFile.basename}]]`;
} else {
    tR += `Keine offene Begegnung für Ort "${ortInput}" gefunden.`;
}
%>