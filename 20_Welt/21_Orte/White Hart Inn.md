---
tags:
  - Ort
Region: "[[Ashabenford]]"
---

## Sinneswahrnehmung

[Kurzbeschreibung]

- *Sehen:* 
	Möbel aus dunklem, polierten Eichenholz 
	An den Wänden hängen Jagdtrophäen, darunter der präparierte Kopf eines weißen Hirsches über dem gewaltigen Kamin
- *Beleuchtung:* Schummrig-gemütlich
	Kamin brennt
- *Hören:* Ein ständiges Grundrauschen aus Gelächter, dem Klappern von Zinnkrügen und dem Knistern des Feuers. Ein Barde spielt meist in der Ecke
- *Riechen:* Eine schwere, aber angenehme Mischung aus gebratenem Fasan (die Spezialität des Hauses), verschüttetem Ale, Pfeifentabak und Holzrauch. 
- *Details:* Die Tische sind massiv und tragen die Schnitzereien von Generationen von Gästen.
	Eine alte Armbrust hängt geladen, aber verstaubt, hinter der Theke ("Friedensstifter")

## POI

#### Der Schankraum 
Der Hauptraum ist fast immer gut gefüllt. An der rechten Wand dominiert der riesige Kamin aus Feldsteinen.
#### Die Theke 
Hier werden lokale Neuigkeiten ausgetauscht. Hinter der Theke lagern Fässer mit *Shadowdale Ale* und *Old Skull*. 
#### Der Ratstisch 
Ein großer Tisch in einer Nische, der traditionell für die Treffen der Ältesten von Ashabenford reserviert ist, wenn sie nicht im Herrenhaus tagen.

## Events

[Was passiert, wenn Bedingung X erfüllt ist?]

## DM Wissen

**Besitzer:** [[Holfast Harpell]] 
	Er ist ein pensionierter Abenteurer und Mitglied des Ältestenrates.
**Besonderheit:** Das Gasthaus ist bekannt für seinen gebratenen Fasan in Kräuterkruste.
**Sicherheit:** Waffen müssen nicht abgegeben werden, aber Holfast duldet keinen Streit. 
	Eine alte Armbrust hängt geladen, aber verstaubt, hinter der Theke ("Friedensstifter").

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
