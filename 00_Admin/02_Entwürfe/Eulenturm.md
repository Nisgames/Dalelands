---
tags:
  - Ort
Region: "[[Cormanthor]]"
---

## Beschreibung

Ein alter Wachturm der [[Myth Drannor Elfen]]. Mittlerweile eine Ruine und unbewohnt.

- Ein etwa 10 m hoher, runder Turm aus hellem Stein.
- Das Wasser des [[Ashaba]] plätschert nur wenige Meter entfernt am Turm vorbei.
- Zum Wasser hin läuft ein kurzer Steg vom Ufer des [[Ashaba]] zu einer hölzernen Tür im Turm.
- In etwa 4 m Höhe ist ein Loch in der Außenwand des Gemäuers. Die Steine sind nach innen eingebrochen an dieser Stelle.

## POI

#### Erdgeschoss

- Runder Raum mit 

## DM Wissen

- Wurde von den [[Myth Drannor Elfen]] errichtet, um reisenden in Not auf dem [[Ashaba]] zu helfen
	- Hier konnten Boote repariert oder Nahrung aufgestockt werden

#### Bewohner
```dataview
table without id file.link as Name
from #NPC and !"00_Admin/03_Templates"
where contains(Ort, this.file.link) 
	and status != "Tot"
sort file.name asc
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
