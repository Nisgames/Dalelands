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
Sprachen:
  - "[[Gemeinsprache]]"
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

- Alter: 15 Jahre
- Größe: 127cm
- lila Haut, goldene Schlangenaugen, gespaltene Zunge
- untere Gesichtshälfte mit Tuch bedeckt 
- heruntergekommene Kleidung

## Hintergrundgeschichte

Jorvan wuchs als Kind in der Trank Brauerei seiner Eltern auf. Mit 8 wurde er von den Yuan Ti entführt und indoctriniert. Aus der Zeit vor seiner Entführung kennt Jorvan nur noch seinen Namen und verschwommene Erinnerungsfetzen.
Die Yuan Ti versklavten ihn aufgrund seiner Herkunft als Gehilfen führ einen ihrer Artificer Alchemisten. Durch das Tüfteln und Experimentieren mit Tränken, was ihn an seine Vergangenheit erinnerte, hielt Jorvan sich seine Persöhnlichkeit so gut es ging zusammen. Nach 3 Jahren stieg er selbst zu einem Vollwertigen Alchemisten Artificer auf, wurde jedoch gezwungener Maßen einem Ritual unterzogen, das ihn zum Yuan Ti machte.
Seine Haut wurde Lila, seine augen zu goldenen Schlangenaugen und seine Zunge spaltete sich.
Nach 4 weiteren Jahren ergab sich endlich die Möglichkeit zur Flucht. Jorvan entkam nur knapp und wurde verfolgt.
In diesem Moment traf er auf [[Tado]] und [[Elina]] die ihm gegen seine Verfolger hielfen. Sie erzählten ihm auch vom Job des Abenteurers, was für ihn der perfekte Job war um stark genug für seine Rache zu werden und gleichzeitig anderen in seiner Lage helfen zu können

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
