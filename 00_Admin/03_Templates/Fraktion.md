---
tags:
  - Fraktion
Gesinnung:
Standorte:
Relevanz:
---

## Agenda

[Großes Ziel]

## Beziehungen

[Hassen Fraktion 2]

## DM Wissen

#### Mitglieder
```dataview
TABLE WITHOUT ID
	file.link as Mitglieder,
	Relevanz as Relevanz
FROM #NPC AND !"3-DM/"
WHERE contains(Fraktionen, this.file.link)
SORT Relevanz ASC
```
