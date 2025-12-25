<%*
// Alle Markdown-Dateien holen
const files = app.vault.getMarkdownFiles().filter(file => {
    const cache = app.metadataCache.getFileCache(file);
    const tags = cache?.tags?.map(t => t.tag) || [];
    const fm = cache?.frontmatter || {};

    // BEDINGUNG: Hat Tag #Zufallsbegegnung UND ist nicht als 'erlebt: true' markiert
    return tags.includes("#Zufallsbegegnung") && fm.erlebt !== true;
});

if (files.length > 0) {
    // Zufällige Datei wählen
    const randomFile = files[Math.floor(Math.random() * files.length)];
    // Fügt den Link zur Notiz ein (als Transklusion mit !)
    tR += `![[${randomFile.basename}]]`;
} else {
    tR += "Keine offenen Zufallsbegegnungen gefunden.";
}
%>
