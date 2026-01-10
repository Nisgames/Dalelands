---
tags:
  - Ort
Region:
---

## Sinneswahrnehmung

[Was hören, sehen, riechen beim Betreten?]

## POI

[Raum 1]

## Events

[Was passiert, wenn Bedingung X erfüllt ist?]

## DM Wissen

[Hintergrund, usw]

#### Bewohner
```dataview
table without id file.link as Name
from #NPC 
where contains(Ort, this.file.link) 
	and status != "Tot"
```
#### Historie
```dataview
list without id link(file.link, title)
from #Session 
where contains(file.outlinks, this.file.link)
```
#### Plot Events