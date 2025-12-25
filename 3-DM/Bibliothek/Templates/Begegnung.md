<%*
const targetTag = "Zufallsbegegnung"; // Dein Tag ohne #

const files = app.vault.getMarkdownFiles().filter(file => {
    const cache = app.metadataCache.getFileCache(file);
    const fm = cache?.frontmatter;

    if (!fm) return false;

    // 1. Tags prüfen (sowohl in Properties als auch im Text)
    // Wir normalisieren alles, um #Zufallsbegegnung und Zufallsbegegnung zu finden
    const frontmatterTags = fm.tags ? (Array.isArray(fm.tags) ? fm.tags : [fm.tags]) : [];
    const textTags = cache.tags ? cache.tags.map(t => t.tag) : [];
    
    // Kombiniere alle Tags und entferne '#' für den Vergleich
    const allTags = [...frontmatterTags, ...textTags].map(t => t.replace('#', ''));
    const hatTag = allTags.includes(targetTag);

    // 2. Erledigt prüfen (Groß-/Kleinschreibung egal)
    // Sucht nach 'Erledigt', 'erledigt', 'Done', etc. falls du es mal änderst
    const istErledigt = fm.Erledigt === true || fm.erledigt === true;

    return hatTag && !istErledigt;
});

if (files.length > 0) {
    const randomFile = files[Math.floor(Math.random() * files.length)];
    tR += `![[${randomFile.basename}]]`;
} else {
    tR += "Keine offenen Begegnungen gefunden.";
}
%>