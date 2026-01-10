---
tags:
  - Fraktion
Gesinnung:
Standorte:
Relevanz:
---

## Generelles

[Logo, Hauptquartier, etc]

## Agenda

[Großes Ziel]

## Beziehungen

[Hassen Fraktion 2]

## DM Wissen

#### Mitglieder
```dataview
TABLE WITHOUT ID
	file.link as "Name",
	rolle as "Rolle",
	ort as "Ort"
FROM #NPC AND !"3-DM/"
WHERE contains(Fraktionen, this.file.link)
SORT Relevanz ASC
```
