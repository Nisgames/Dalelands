---
tags:
  - Gruppierung
  - Fraktion
Gesinnung: Böse
Standorte:
  - "[[Dalelands]]"
Relevanz: Hoch
---

## Generelles

Eine mächtige Söldner- und Händlerorganisation. Sie sind überall. 
Sie bieten Schutz gegen Gold. 
Viele misstrauen ihnen, aber ohne ihre Karawanen würde der Handel zusammenbrechen.
Man arbeitet mit ihnen, aber man dreht ihnen nie den Rücken zu.

![[Pasted image 20260113145926.png|right|150]]

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