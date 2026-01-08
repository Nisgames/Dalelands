---
tags:
  - Gruppierung
Gesinnung:
Standorte:
Relevanz:
---
# `=this.file.name` 

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
