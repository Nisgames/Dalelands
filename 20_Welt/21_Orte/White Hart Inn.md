---
tags:
  - Ort
Region: "[[Ashabenford]]"
---

## Sinneswahrnehmung

[Was hören, sehen, riechen beim Betreten?]

- *Sehen:* 
- *Beleuchtung:* 
- *Hören:* 
- *Riechen:* 
- *Spüren:* 
- *Atmosphäre:* 
- *Details:* 

- *Sehen:* 
	Möbel aus dunklem, polierten Eichenholz 
	An den Wänden hängen Jagdtrophäen, darunter der präparierte Kopf eines weißen Hirsches über dem gewaltigen Kamin
- *Beleuchtung:* Schummrig-gemütlich
	Kamin brennt
- *Hören:* Ein ständiges Grundrauschen aus Gelächter, dem Klappern von Zinnkrügen und dem Knistern des Feuers. Ein Barde spielt meist in der Ecke (aktuell versucht er, den Lärm zu übertönen). 
- *Riechen:* Eine schwere, aber angenehme Mischung aus gebratenem Fasan (die Spezialität des Hauses), verschüttetem Ale, Pfeifentabak und Holzrauch. 
- *Details:* Die Tische sind massiv und tragen die Schnitzereien von Generationen von Gästen.
## POI

[Raum 1]

## Events

[Was passiert, wenn Bedingung X erfüllt ist?]

## DM Wissen

[Hintergrund, usw]

#### Bewohner
```dataview
table without id file.link as Name
from #NPC and !"00_Admin/03_Templates"
where contains(Ort, this.file.link) 
	and status != "Tot"
```
#### Historie
```dataview
list without id link(file.link, title)
from #Session and !"00_Admin/03_Templates"
where contains(file.outlinks, this.file.link)
```
#### Plot Events
```dataview
task 
from #Plot and !"00_Admin/03_Templates"
where contains(tags, "#loc/" + this.file.name)
	and !resolved
```
