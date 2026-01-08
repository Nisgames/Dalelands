---
tags:
  - Gruppierung
Gesinnung:
Standorte:
Relevanz:
---
# `=this.file.name` 

### Mitglieder

```dataview
TABLE WITHOUT ID
	file.link as Mitglieder,
	Relevanz as Relevanz
FROM #NPC AND !"3-DM/"
WHERE contains(Fraktionen, this.file.link)
SORT Relevanz ASC
```
