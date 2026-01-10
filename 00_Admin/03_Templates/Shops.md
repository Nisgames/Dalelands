---
tags:
  - Ort
Region: 
Besitzer: 
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

## POI

[Raum 1]

## Events

[Was passiert, wenn Bedingung X erfüllt ist?]

## DM Wissen

[Besitzer]
[Einfache Waffen und Rüstungen]
[Keine Schilde]
[Kauft zu 70% des Wertes an]
[Hintergrund, usw]

#### Angebot (Exklusiv)
```dataview
table without id
	file.link as "Item",
	Wert_in_GM as "Preis",
	seltenheit as "Seltenheit"
from #Item 
where contains(ort, this.file.link)
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
