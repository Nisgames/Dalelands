---
tags:
  - PC
Volk: Zwerg
Klasse: Paladin 2, Hexenmeister 1
hp: "1"
ac: "19"
level: 3
modifier: 0
Spieler: "[[Liam]]"
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
