---
tags:
  - Ort
Liegt_in: "[[Faerûn]]"
Fraktionen: "[[4-Faerûn/Gruppierungen/Zhentarim]]"
---

## 📖 Allgemeinwissen

## Bewohner
```dataview
TABLE WITHOUT ID
	file.link as Name,
	Relevanz as Relevanz
from #NPC 
where contains(Wohnort, this.file.link)
```
