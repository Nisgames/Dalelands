---
tags:
  - PC
Volk: Yuan-Ti
Klasse: Magieschmied
hp: "25"
ac: "18"
level: 3
modifier: 0
Spieler: "[[Mika]]"
---

# Sessions
### Teilgenommen
```dataview
TABLE WITHOUT ID
	file.link as Session,
	DM as DM,
	date as Datum
FROM #Session AND !"3-DM"
WHERE
	contains(Players, this.file.link)
SORT date ASC
```
### Nicht teilgenommen
```dataview
TABLE WITHOUT ID
	file.link as Session,
	DM as DM,
	date as Datum
FROM #Session AND !"3-DM"
WHERE
	!contains(Players, this.file.link)
SORT date ASC
```
