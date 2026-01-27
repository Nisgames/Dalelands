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
	- An der Stelle wo das Herz
## POI

Der dichte Wald lichtet sich abrupt. Vor euch liegt ein kreisrundes Plateau, umringt von uralten Eichen, deren Blätter hier nicht herbstlich rot, sondern schneeweiß sind.

In der Mitte steht ein offener Pavillon aus weißem Marmor. Schlanke Säulen ragen in den grauen Himmel, teilweise von Efeu überwuchert, der leise violett schimmert.

In der Mitte des Pavillons steht eine Statue: Eine Elfe, die eine Harfe spielt. Doch der Kopf der Statue fehlt. Dort, wo das Herz der Statue wäre, pulsiert ein Licht. Es ist der [[Schattensplitter]]. Er steckt tief im Marmor.

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
