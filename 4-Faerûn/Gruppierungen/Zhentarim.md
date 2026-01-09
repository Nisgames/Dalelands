---
tags:
  - Gruppierung
Gesinnung: Böse
Standorte:
  - "[[Dalelands]]"
Relevanz: Hoch
---
# `=this.file.name` 

Eine mächtige Söldner- und Händlerorganisation. Sie sind **überall**. Sie bieten Schutz gegen Gold. Viele misstrauen ihnen, aber ohne ihre Karawanen würde der Handel zusammenbrechen. Man arbeitet mit ihnen, aber man dreht ihnen nie den Rücken zu.

### Mitglieder

```dataview
TABLE WITHOUT ID
	file.link as Mitglieder,
	Relevanz as Relevanz
FROM #NPC 
WHERE contains(Fraktionen, this.file.link)
SORT Relevanz ASC
```
