---
tags:
  - Ort
  - Dale
Region: "[[Dalelands]]"
---

## Sinneswahrnehmung

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

## Events

[Was passiert, wenn Bedingung X erfüllt ist?]

## DM Wissen

Gilt als militaristisch, humorlos und unfreundlich. 
"Die laufen in Rüstung zum Frühstück." 
Man ist froh, im freien Mistledale zu leben.

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
