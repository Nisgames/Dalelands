---
tags:
  - Ort
Liegt_in:
Fraktionen:
---

## 📖 Allgemeinwissen

Das reiche Nachbarland im Süden rüstet auf. Händler erzählen von neuen Zöllen und Soldatenbewegungen.
Händler von dort gelten als gierig und verschlagen. 
"Zähl deine Finger nach, wenn du einem Sembianer die Hand geschüttelt hast."

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
from #NPC AND !"3-DM/"
where contains(Wohnort, this.file.link)
```
