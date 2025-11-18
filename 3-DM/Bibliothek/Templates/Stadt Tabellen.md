### Wichtige Personen
```dataview
TABLE WITHOUT ID
	file.name as "Name",
	Volk, 
	Klasse
FROM #NPC 
WHERE contains([this.file.link], Wohnort)
AND contains(["Hoch"], Relevanz)
SORT Name ASC 
```
### Bewohner
```dataview
TABLE WITHOUT ID
	file.link AS "Name",
	Volk, 
	Klasse
FROM #NPC 
WHERE contains([this.file.link], Wohnort)
SORT file.link ASC
```
### Orte
```dataview
TABLE WITHOUT ID
	file.link AS "Ort",
	filter(tags, (t) => !contains("#Ort", t)) AS "Art"
FROM #Ort
WHERE Liegt_in = [this.file.link]
SORT file.name ASC
```
