---
tags:
  - Ort
Liegt_in:
Fraktionen:
---
---
### Bewohner
```dataview
TABLE WITHOUT ID
	file.link as Name,
	Relevanz as Relevanz
from #NPC 
where contains(Wohnort, this.file.link)
```
## 📰 Aktuelle Gerüchte & Plot-Hooks
```dataview
TABLE WITHOUT ID 
file.link AS "Plot",
regexreplace(Rows.text, "\[\[.*?\]\]", "") AS "Was passiert hier?"
FROM "3-DM/Quests"
FLATTEN file.lists AS Rows
WHERE contains(Rows.outlinks, this.file.link) AND file.frontmatter.resolved
```
