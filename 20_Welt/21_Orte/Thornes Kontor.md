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

#### Der Verkaufsraum (EG)
* Regale voller "legitimer" Waren: Seide aus Sembia, Weine aus dem Süden, hochwertiges Werkzeug.
* Hier empfängt Gideon normale Kunden. Alles wirkt extrem ordentlich.

####Gideons Büro (OG)**
* Erreichbar über eine enge Wendeltreppe.
* Luxuriös eingerichtet: Bärenfell vor dem Kamin, Mahagoni-Schreibtisch, eine Wand voller Landkarten der Dalelands.
* **Geheimnis:** Hinter einer Karte von Cormanthor befindet sich ein Wandtresor (DC 15 Untersuchung, DC 20 Schlossknacken). Inhalt: Echtes Gold, Zhentarim-Briefe und ggf. ein [[Schattensplitter]].

**3. Das "Nasse Lager" (Untergeschoss/Flussebene)**
* Ein geheimer Bereich unter dem Hauptboden, zwischen den Stützpfeilern.
* **Zugang:** Eine Falltür unter einem Teppich im Büro oder direkt vom Fluss aus (nur bei Ebbe oder per Boot).
* Hier lagert die Schmuggelware (Waffen, Gifte, und die Kisten mit [[Schattensplitter]]n).
* Ein kleines Ruderboot ist hier immer vertäut, bereit für eine schnelle Flucht.

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
