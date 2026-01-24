---
tags:
  - Ort
Region: "[[Cormanthor]]"
---

## Beschreibung

Der weiße Hain war einst ein offener Pavillon der Elfen 
Ein Ort der Kunst und Musik, bestehend aus weißen Marmorsäulen unter freiem Himmel

- [Sehen / Licht] 
- [Hören] 
- [Riechen / Temperatur] 
- [Stimmung]

## POI

- [Interaktives Element 1] 
- [Interaktives Element 2]

## DM Wissen

[Hintergrund, usw]

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
