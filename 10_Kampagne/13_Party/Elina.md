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

#### Merkmale
- realtiv misstrauisch 
- bischen verrückt 
- will gutes tun
#### Ideale
- eine Welt, in der Unschuldige nicht versklavt werden (siehe [[Jorvan#Hintergrundgeschichte|Hintergrundgeschichte]])
#### Bindungen
- Rache an den Yuan Ti
#### Makel
- Indoktrination der Yuan Ti hat sein Verständnis von Gut und Böse verschwimmen lassen
#### Feinde
- Yuan Ti Zivilisation

## Aussehen

- normale Statur, sportlich
- offene, wellige Haare
- spitze Ohren (Elf)
###### Frühling
- braune Haare, grüne Augen
###### Sommer

###### 

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
