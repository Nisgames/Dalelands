---
tags:
  - Gruppierung
  - Gilde
Leitung: "[[Ester]]"
Liegt in: "[[Silberquell]]"
---
---

# Questboard
```dataview
TABLE WITHOUT ID
	file.link AS "Quest",
	Auftraggeber,
	Belohnung
FROM #Quest 
WHERE contains([this.file.link], Gilde)
	AND file.name != "Quest"
	AND Erledigt = false
```
---

# Mitglieder
```dataview
TABLE WITHOUT ID
	file.link as "Name"
FROM #NPC 
WHERE
	contains(Fraktionen, this.file.link)
	AND Fraktionen
SORT file.link ASC
```
