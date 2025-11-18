---
tags:
  - PC
Volk: Seaturtle
Klasse: Kämpfer
hp: 1
ac: 1
level: 3
modifier: 0
Spieler: "[[Alina]]"
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
