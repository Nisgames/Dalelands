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
FROM #NPC 
WHERE contains(Fraktionen, this.file.link)
```
