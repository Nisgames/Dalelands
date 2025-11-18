---
tags:
  - Ort
  - Stadt
Liegt_in:
  - "[[Iteron]]"
Fraktionen:
  - "[[Stadtwache Silberquell]]"
---
---

### Geographische Lage
- Grenzt südwestlich an einen großen Wald
- Nordosten ist ein großer See
	- Hafen von Silberquell

### Beschreibung
- Sehr große Stadt
- Riesiger Markt direkt am Stadttor - Bekannt dafür, dass man fast alles irgendwo finden kann
- Brunnen in der Stadtmitte
	- Herkunft "Silberquell"

- [[König Panda]] 
- [[Ester]] 
- Richter
- Stadtwache
- Händler und Ladenbesitzer

### Wichtige Personen
```dataview
TABLE WITHOUT ID
	file.name as "Name",
	Volk, 
	Klasse
FROM #NPC 
WHERE contains(this.file.link, Wohnort)
AND contains(Relevanz, "Hoch")
SORT Name ASC 
```
### Bewohner
```dataview
TABLE WITHOUT ID
	file.link AS "Name",
	Volk, 
	Klasse
FROM #NPC 
WHERE contains(Wohnort, this.file.link)
SORT file.link ASC
```
### Orte
```dataview
TABLE WITHOUT ID
	file.link AS "Ort",
	filter(tags, (t) => !contains("#Ort", t)) AS "Art"
FROM #Ort
WHERE contains(Liegt_in, this.file.link)
SORT tags, file.name ASC
```
