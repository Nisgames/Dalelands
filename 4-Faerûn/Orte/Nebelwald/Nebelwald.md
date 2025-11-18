---
tags:
  - Ort
  - Dorf
Liegt_in:
  - "[[Iteron]]"
Fraktionen:
  - "[[Lila-Drachen-Gilde]]"
---
---
# Nebelwald
*Veraltet*
Ein kleines Dorf mit schätzungsweise 3 dutzend Häusern. Es ist umgeben von Feldern. Schon aus der Ferne sticht der verhältnismäßig hohe Kirchturm euch ins Auge, auf dessen Spitze eine blühende Rose und eine Getreideähre zu sehen sind. Man hört ständig geschäftiges Arbeiten.

**Neu**
Nebelwald ist komplett zerstört. Die Häuser sind abgebrannt und eingestürzt und kaum ein Stein steht noch auf dem anderen.

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
