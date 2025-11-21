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
