---
tags:
  - Gruppierung
Gesinnung: Böse
Standorte:
  - "[[Aencar's Manor]]"
Relevanz: Hoch
---
# `=this.file.name` 
## Allgemeinwissen

Alte Schauergeschichten erzählen von Verrückten, die Drachen anbeten. 
Manchmal sieht man seltsame Blitze über dem verlassenen Anwesen des alten Mantelkönigs ([[Aencar's Manor]]) in [[Battledale]].

## 📰 Aktuelle Gerüchte & Plot-Hooks
```dataview
TABLE WITHOUT ID 
file.link AS "Plot",
regexreplace(Rows.text, "\[\[.*?\]\]", "") AS "Was passiert hier?"
FROM #Plot 
FLATTEN file.lists AS Rows
WHERE contains(Rows.outlinks, this.file.link) AND !file.frontmatter.resolved
```

## Mitglieder

```dataview
TABLE WITHOUT ID
	file.link as Mitglieder,
	Relevanz as Relevanz
FROM #NPC AND !"3-DM/"
WHERE contains(Fraktionen, this.file.link)
SORT Relevanz ASC
```
