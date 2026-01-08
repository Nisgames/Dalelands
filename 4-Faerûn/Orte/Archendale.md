---
tags:
  - Ort
Liegt_in: "[[Dalelands]]"
Fraktionen:
---

## 📖 Allgemeinwissen

Gilt als militaristisch, humorlos und unfreundlich. 
"Die laufen in Rüstung zum Frühstück." 
Man ist froh, im freien Mistledale zu leben.

## Bewohner
```dataview
TABLE WITHOUT ID
	file.link as Name,
	Relevanz as Relevanz
from #NPC 
where contains(Wohnort, this.file.link)
```
