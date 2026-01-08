---
tags:
  - Ort
  - Fluss
Liegt_in: "[[Mistledale]]"
Fraktionen:
---
## 📖 Allgemeinwissen

Ein sehr langer Fluss quer durch die Dalelands. 
Die Lebensader der Region. 
Er fließt aus den Tiefen des [[Cormanthor]]-Waldes heraus. 
In letzter Zeit spült er manchmal tote, seltsam verformte Fische an.

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
