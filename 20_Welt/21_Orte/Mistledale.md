---
tags:
  - Ort
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

Mistledale hat keine große Armee, aber die **"Reiter von Mistledale"** (Riders of Mistledale).
Das ist eine sehr fähige Miliz zu Pferd. 
Sie patrouillieren die Straßen. 
Wenn es Ärger gibt, ruft man nach den Reitern, nicht der Stadtwache (die gibt es kaum).

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
