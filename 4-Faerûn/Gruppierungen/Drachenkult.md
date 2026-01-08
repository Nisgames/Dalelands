---
tags:
  - Gruppierung
Gesinnung: Böse
Standorte:
  - "[[Aencar's Manor]]"
Relevanz: Hoch
---
# `=this.file.name` 

### Mitglieder

```dataview
TABLE WITHOUT ID
	file.link as Mitglieder,
	Relevanz as Relevanz
FROM #NPC and 3-DM/Bibliothek/Templates
WHERE contains(Fraktionen, this.file.link)
SORT Relevanz ASC
```
