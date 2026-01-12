---
tags:
  - PC
Volk: Zwerg
Klasse: Paladin 2, Hexenmeister 1
hp: "25"
ac: "19"
level: 3
modifier: 0
Spieler: "[[Liam]]"
---

## Persönlichkeit

- [Noch in Arbeit]

## Aussehen

- Alter: 110 Jahre
- Größe: 138cm
- 

## Hintergrundgeschichte

- [Noch in Arbeit]

## Sessions
#### Teilgenommen
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
#### Nicht teilgenommen
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
