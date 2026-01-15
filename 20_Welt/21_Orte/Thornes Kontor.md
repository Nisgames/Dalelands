---
tags:
  - Ort
  - Gebäude
Region: "[[Ashabenford]]"
---

## Beschreibung

> [!narrator] Außenansicht
> Das Kontor ragt halb über das Wasser hinaus, gestützt von massiven, algenbewachsenen Holzpfählen.
> Im Erdgeschoss herrscht geschäftiges Treiben – Arbeiter verladen Kisten auf flache Flusskähne.
> Im oberen Stockwerk, mit Blick auf den Fluss, brennt warmes Licht in einem großen Erkerfenster.

- *Sehen:* 
	Ein großes, zweistöckiges Gebäude direkt am Ufer des [[Ashaba]] Flusses, am östlichen Rand von Ashabenford.
	Das Schild über der Tür zeigt eine Waage, auf der eine Feder und eine Goldmünze im Gleichgewicht sind.
- *Beleuchtung:* 
	
- *Hören:* 
	
- *Riechen:* 
	Es riecht nach exotischen Gewürzen, Sägemehl und feuchtem Flusswasser.
- *Spüren:* 
	
- *Atmosphäre:* 
	
- *Details:* 
	

## POI

[Raum 1]

## Events

[Was passiert, wenn Bedingung X erfüllt ist?]

## DM Wissen

[Hintergrund, usw]

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
