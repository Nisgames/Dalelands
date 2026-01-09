<%*
const targetTag = "Zufallsbegegnung"; 
const templateFolder = "Templates";

// Hilfsfunktion: Prüfen, ob eine Datei verlinkt ist (Backlinks checken)
function istVerlinkt(filePath) {
    const allLinks = app.metadataCache.resolvedLinks;
    for (const sourcePath in allLinks) {
        // Links aus dem Template-Ordner ignorieren wir
        if (sourcePath.includes(templateFolder)) continue;
        
        // Wenn in irgendeiner Datei ein Link zu unserem Ziel existiert:
        if (allLinks[sourcePath][filePath]) {
            return true;
        }
    }
    return false;
}

// 1. Daten sammeln
const entries = app.vault.getMarkdownFiles().map(file => {
    const cache = app.metadataCache.getFileCache(file);
    const fm = cache?.frontmatter;
    
    const fmTags = fm?.tags ? (Array.isArray(fm.tags) ? fm.tags : [fm.tags]) : [];
    const txtTags = cache?.tags ? cache.tags.map(t => t.tag) : [];
    const allTags = [...fmTags, ...txtTags].map(t => t.replace('#', ''));
    
    return {
        file: file,
        tags: allTags,
        // Prüfen ob verlinkt ODER Checkbox gesetzt (optional, falls du alte manuell abhaken willst)
        schonBenutzt: istVerlinkt(file.path) || (fm?.Erlebt === true),
        isTemplate: file.path.includes(templateFolder)
    };
});

// 2. Filtern: Nur unverlinkte Kandidaten
const candidates = entries.filter(e => 
    e.tags.includes(targetTag) && !e.schonBenutzt && !e.isTemplate
);

// 3. Orte extrahieren
const ortSet = new Set();
candidates.forEach(e => {
    e.tags.forEach(tag => {
        if (tag !== targetTag) ortSet.add(tag);
    });
});
const orte = Array.from(ortSet).sort();
const auswahlOptionen = ["Alle Orte", ...orte];

// 4. Auswahl
const wahl = await tp.system.suggester(auswahlOptionen, auswahlOptionen);

if (wahl) {
    const pool = (wahl === "Alle Orte") 
        ? candidates 
        : candidates.filter(e => e.tags.includes(wahl));

    if (pool.length > 0) {
        const randomEntry = pool[Math.floor(Math.random() * pool.length)];
        // Wir setzen KEINEN Haken mehr, das Einfügen des Links reicht als "Erlebt" Markierung
        tR += `![[${randomEntry.file.basename}]]`;
    } else {
        tR += `Keine unbenutzten Begegnungen für "${wahl}" gefunden.`;
    }
}
%>