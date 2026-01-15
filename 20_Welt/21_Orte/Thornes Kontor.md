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
* Regale voller "legitimer" Waren: Seide aus [[Sembia]], Weine aus dem Süden, hochwertiges Werkzeug.
* Alles wirkt extrem ordentlich.
* Hier empfängt Gideon normale Kunden.

#### Gideons Büro (OG)
* Erreichbar über eine enge Wendeltreppe.
* Luxuriös eingerichtet: Bärenfell vor dem Kamin, Mahagoni-Schreibtisch, eine Wand voller Landkarten der Dalelands.
* **Geheim:** Hinter einer Karte von [[Cormanthor]] befindet sich ein Wandtresor (DC 15 Untersuchung, DC 20 Schlossknacken). Inhalt: Echtes Gold, [[Zhentarim]]-Briefe und ggf. ein [[Schattensplitter]].

#### Das "Nasse Lager" (Untergeschoss/Flussebene)
* Ein geheimer Bereich unter dem Hauptboden, zwischen den Stützpfeilern.
* **Zugang:** Eine Falltür unter einem Teppich im Büro oder direkt vom Fluss aus (nur bei Ebbe oder per Boot).
* Hier lagert die Schmuggelware (Waffen, Gifte, und die Kisten mit [[Schattensplitter]]n).
* Ein kleines Ruderboot ist hier immer vertäut, bereit für eine schnelle Flucht.

## Events

[Was passiert, wenn Bedingung X erfüllt ist?]

## DM Wissen

* **Sicherheit:** Nachts patrouillieren hier 2 **Wachhunde** (Mastiffs) und ein Söldner (Loyalität gilt dem Gold).
* **Die Falle:** Die Treppe zum Büro kann manipuliert werden (Hebel unter dem Schreibtisch), um sich in eine Rutsche zu verwandeln (DC 15 Wahrnehmung). Wer darauf steht, rutscht direkt durch eine Klappe ins kalte Flusswasser – oder in ein Netz im "Nassen Lager".
* **Akustik:** Das Büro ist schallgedämpft. Schreie dringen nicht nach unten in den Verkaufsraum.

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
