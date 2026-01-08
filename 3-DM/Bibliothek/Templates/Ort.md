---
tags:
  - Ort
Liegt_in:
Fraktionen:
---
---

## 📰 Aktuelle Gerüchte & Plot-Hooks
```dataview
TABLE WITHOUT ID 
file.link AS "Plot",
regexreplace(Rows.text, "\[\[.*?\]\]", "") AS "Was passiert hier?"
FROM #Plot 
FLATTEN file.lists AS Rows
WHERE contains(Rows.outlinks, this.file.link) AND !file.frontmatter.resolved
```

## Bewohner
```dataview
TABLE WITHOUT ID
	file.link as Name,
	Relevanz as Relevanz
from #NPC 
where contains(Wohnort, this.file.link)
```
