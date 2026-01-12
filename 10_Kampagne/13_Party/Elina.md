---
tags:
  - PC
Volk: Eladrin
Klasse: Waldläuferin
hp: "25"
ac: "14"
level: 3
modifier: 0
Spieler: "[[Alina]]"
---

## Persönlichkeit

- Je nach Jahreszeit ihrer Eladrin-Herkunft

## Aussehen

- normale Statur, sportlich
- offene, wellige Haare
- spitze Ohren (Elf)
###### Frühling
- braune Haare, grüne Augen
###### Sommer
- goldene Haare, grüne Augen
###### Herbst
- orangene Haare, rötliche Augen, dunklere Haut
###### Winter
- weiße Haare, blaue Augen, helle Haut

## Hintergrundgeschichte



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
