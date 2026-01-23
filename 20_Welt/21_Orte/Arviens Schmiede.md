---
tags:
  - Ort
Region: "[[Ashabenford]]"
---

## Beschreibung

Einzige Schmiede in [[Ashabenford]]. Eigentlich spezialisiert auf Zinn- und Kupferarbeiten sowie Werkzeuge für Bauern, wird aber oft von Abenteurern zu Waffenreparaturen genötigt.

- Eine offene Werkstadt 
- Schwerter, Rüstungen und Werkzeuge an den Wänden
- Sehr laut und heiß aufgrund der Öfen

## POI

#### Waffen an den Wänden

- Schwerter, Dolche, Hellebarden, aber auch Äxte, Sensen und Sägen
- Hier und da stehen Rüstungen, die sehr schwer und teuer aussehen

#### Hochofen

- Hier ist [[Arvien]] meist zugange
- Glühendes Metall wird unter lautem Hämmern auf einem Amboss ge

## DM Wissen

Hier könnten +1 Waffen und Wüstungen gefertigt werden. _Benötigtes Material: [[Mithral]]_ 

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
