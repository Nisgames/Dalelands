<%*
const targetTag = "Zufallsbegegnung"; 
const templateFolder = "Templates"; // Dein Template-Ordner

// 1. Alle Dateien scannen und relevante Daten (Tags/Status) vorab sammeln
const entries = app.vault.getMarkdownFiles().map(file => {
    const cache = app.metadataCache.getFileCache(file);
    const fm = cache?.frontmatter;
    
    // Tags aus Frontmatter und Text sammeln & bereinigen
    const fmTags = fm?.tags ? (Array.isArray(fm.tags) ? fm.tags : [fm.tags]) : [];
    const txtTags = cache?.tags ? cache.tags.map(t => t.tag) : [];
    const allTags = [...fmTags, ...txtTags].map(t => t.replace('#', ''));
    
    return {
        file: file,
        tags: allTags,
        erledigt: fm?.Erledigt === true || fm?.erledigt === true,
        isTemplate: file.path.includes(templateFolder)
    };
});

// 2. Filtern: Nur offene Zufallsbegegnungen
const candidates = entries.filter(e => 
    e.tags.includes(targetTag) && !e.erledigt && !e.isTemplate
);

// 3. Verfügbare Orte aus den Kandidaten extrahieren
const ortSet = new Set();
candidates.forEach(e => {
    e.tags.forEach(tag => {
        if (tag !== targetTag) ortSet.add(tag); // Ziel-Tag selbst ignorieren
    });
});
const orte = Array.from(ortSet).sort();
const auswahlOptionen = ["Alle Orte", ...orte];

// 4. Auswahlmenü anzeigen
const wahl = await tp.system.suggester(auswahlOptionen, auswahlOptionen);

if (wahl) {
    // Liste nach Wahl filtern (oder alle nehmen)
    const pool = (wahl === "Alle Orte") 
        ? candidates 
        : candidates.filter(e => e.tags.includes(wahl));

    if (pool.length > 0) {
        const randomEntry = pool[Math.floor(Math.random() * pool.length)];
        tR += `![[${randomEntry.file.basename}]]`;
    } else {
        tR += `Keine Begegnungen für "${wahl}" gefunden.`;
    }
} else {
    // Falls ESC gedrückt wurde
    tR += ""; 
}
%>