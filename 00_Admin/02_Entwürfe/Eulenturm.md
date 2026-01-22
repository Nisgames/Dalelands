---
tags:
  - Ort
Region: "[[Cormanthor]]"
---

## Beschreibung

Ein alter Wachturm der [[Myth Drannor Elfen]]. Mittlerweile eine Ruine und unbewohnt.

- Ein etwa 10 m hoher, runder Turm aus hellem Stein. Er wird umarmt vom Astwerk eines großen Baumes.
- Das Wasser des [[Ashaba]] plätschert nur wenige Meter entfernt am Turm vorbei.
- Zum Wasser hin läuft ein kurzer Steg vom Ufer des [[Ashaba]] zu einer hölzernen Tür im Turm.
- In etwa 4 m Höhe ist ein Loch in der Außenwand des Gemäuers. Die Steine sind nach innen eingebrochen an dieser Stelle.

## POI

#### Erdgeschoss

- Vollgestellt mit großen Holzkisten
	- Größtenteils leer (*vielleicht geplündert?*)
	- Hier und da Seile (4 m Stücke) oder Kupferringe in verschiedenen Größen
- Karten von [[Cormanthor]] an den Wänden
	- Zeigen Verlauf des [[Ashaba]] und mögliche Gefahrenstellen (Strömungen, flache Stellen)
- Hinten im Raum Wendeltreppe nach oben
- Scherben von zerbrochenen Tonkrügen auf den Boden
- Fenster mit Blick in den Wald

#### 1. Stock

- Großer Steintisch mitten im Raum. Darauf liegen umgekippte Silberbecher (7) und ein paar verstreute Würfel (5)
	- Grobe Holzstühle drum herum
	- Am Kopfende ein besonders verzierter Becher (nicht gerostet)
		- [[Everclean Becher]] 
- Stein-Nischen in den Wänden; haben früher als Regale gedient
	- *Nachforschungen:* 
		Eine alte Tachenuhr (stehengeblieben)
		Ein bronzefarbener Dolch mit verziertem Griff
		Versteckter Stein-Knopf in einem der Fächer (Nahe Wendeltreppe)
			*Schiebt Wandstück an der Wendeltreppe nach unten vor - Man kommt nicht mehr nach unten, bis erneut gedrückt wird*
- Hölzerner Schrank an gegenüberliegender Wand
	- Verschlossen - *Athletik DC 12 zum aufbrechen*
		- Ein enormer Gestank kommt entgegen
		- Auf dem Boden des Schranks liegen 2 tote Fledermäuse

#### 2. Stock

- An mehreren Stellen wurde Stroh zu Betten zusammengeschoben
	- Hier scheinen früher Wachen geschlafen zu haben
- Ein Spiegel in hübsch verziertem Rahmen hängt an der Wand
	- Extrem verstaubt - Man müsste ihn polieren
- Fenster haben kleine Landeflächen für Vögel (Eulen)
	- *Geschichte DC 12: Von hier wurden früher Nachrichten per Eulen versendet und Druiden empfangen*

## DM Wissen

- Wurde von den [[Myth Drannor Elfen]] errichtet, um reisenden in Not auf dem [[Ashaba]] zu helfen
	- Hier konnten Boote repariert oder Nahrung aufgestockt werden
- Bei Verdacht wurde auch die ein oder andere Ladung der Händler kontrolliert und im Zweifel einkassiert um Schmuggel zu verhindern

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
