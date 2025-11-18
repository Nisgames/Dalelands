---
tags:
  - PC
Volk: Tiefling
Klasse: Barde
hp: 26
ac: 13
level: 4
modifier: 0
Spieler: "[[Leif]]"
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
