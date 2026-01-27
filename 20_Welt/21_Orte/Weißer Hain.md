---
tags:
  - Ort
Region: "[[Cormanthor]]"
---

## Beschreibung

Der weiße Hain war einst ein offener Pavillon der Elfen 
Ein Ort der Kunst und Musik, bestehend aus weißen Marmorsäulen unter freiem Himmel

- Kreisrundes Plateau aus Marmor
- Umringt von uralten Eichen
	- Nicht herbstlich rot, sondern schneeweiß
- Offener Pavillon in der mitte von schlanken Säulen umringt
	- Teilweise von Efeu überwuchert, der violett schimmert
- In der Mitte des Pavillons steht eine Statue: Eine Elfe, die Harfe spielt
	- Kopf der Statue fehlt
	- An der Stelle wo das Herz wäre, pulsiert ein [[Schattensplitter]]
	- Er steckt tief im Marmor
## POI

- 

## DM Wissen

Einst ein romantischer Ort der Kunst und Musik für die [[Myth Drannor Elfen]] 

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
