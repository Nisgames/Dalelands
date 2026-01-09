---
tags:
  - Ort
Liegt_in:
Fraktionen:
---

## 📖 Allgemeinwissen


## Bewohner
```dataview
TABLE WITHOUT ID
	file.link as Name,
	Relevanz as Relevanz
from #NPC AND !"3-DM/"
where contains(Wohnort, this.file.link)
```
