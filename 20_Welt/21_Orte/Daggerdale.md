---
tags:
  - Ort
  - Dale
Region: "[[Dalelands]]"
---

## Beschreibung

[Kurzbeschreibung]

- *Sehen:* 
	
- *Beleuchtung:* 
	
- *Hören:* 
	
- *Riechen:* 
	
- *Spüren:* 
	
- *Atmosphäre:* 
	
- *Details:* 
	

## POI

[Raum 1]

## DM Wissen

#### Zhentarim

Die [[Zhentarim]] werden in [[Daggerdale]] meistens als die Guten dargestellt. Es wird Propaganda verbreitet, das die [[Zhentarim]] die Bew

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
