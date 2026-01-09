---
tags:
  - Ort
Liegt_in:
Fraktionen:
---

## 📖 Allgemeinwissen

Mistledale hat keine große Armee, aber die **"Reiter von Mistledale"** (Riders of Mistledale).
Das ist eine sehr fähige Miliz zu Pferd. 
Sie patrouillieren die Straßen. 
Wenn es Ärger gibt, ruft man nach den Reitern, nicht der Stadtwache (die gibt es kaum).

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
