---
tags:
  - Ort
  - Wald
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

## Events

[Was passiert, wenn Bedingung X erfüllt ist?]

## DM Wissen

Der gigantische Wald, der die Täler umgibt. Früher die Heimat der Elfen, heute ein gefährliches Niemandsland.

"Bleib auf den Wegen." Wer tief ins Dickicht geht, kommt selten zurück. Es heißt, seit dem Absturz seien die Tiere aggressiver geworden.

Die Drow: Es ist ein offenes Geheimnis, dass Dunkelelfen (Drow) die Schatten des Waldes nutzen, um Überfälle zu begehen. Man fürchtet sie, sieht sie aber selten.

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
