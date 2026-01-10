---
tags:
  - Fraktion
Gesinnung: 
Standorte:
Relevanz:
---

## Generelles

Alte Schauergeschichten erzählen von Verrückten, die Drachen anbeten. 
Manchmal sieht man seltsame Blitze über dem verlassenen Anwesen des alten Mantelkönigs ([[Aencar's Manor]]) in [[Battledale]].

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
FROM #NPC AND !"00_Admin/03_Templates"
WHERE contains(Fraktionen, this.file.link)
SORT rolle ASC
```
#### Plots
```dataview
table without id file.link as "Plot", category as "Kategorie"
from #Plot and !"00_Admin/03_Templates"
where contains(file.outlinks, this.file.link)
sort category asc
```