---
tags:
  - Ort
  - Fluss
Region: "[[Dalelands]]"
---

## Sinneswahrnehmung

Der **Ashaba** ist die wichtigste Wasserader der [[Dalelands]], windet sich von den [[Desertsmouth Mountains]] bis hinunter zur [[Dragon Reach]]. 
Für die Bewohner ist er Trinkwasserquelle, Waschplatz und Transportweg zugleich – auch wenn er tückischer ist, als er aussieht.

- *Sehen:* 
	Dunkles, klares Wasser mit steinigem Grund
	**Tiefe:** Durchschnittlich nur 2-3 Meter, oft flacher.
	**Breite:** Unterschiedlich; Durchschnittlich 20-30m
- *Hören:* 
	Stetiges Rauschen und Plätschern
- *Riechen:* 
	Nach kaltem Stein, Algen und im Herbst oft nach faulendem Laub, das aus den Wäldern geschwemmt wird.
- *Spüren:* 
	Selbst im Sommer eiskalt.
- *Atmosphäre:* 
	Der Fluss wirkt uralt und gleichgültig. Er war schon da, bevor die Menschen kamen, und er wird noch fließen, wenn sie weg sind.
- *Details:* 
	Trügerisch starke Strömung in der Mitte

## POI

#### Die Furt von [[Ashabenford]] 
Die bekannteste flache Stelle (siehe [[Ashabenford]]). Hier müssen Boote oft entladen oder über die Steine gezogen werden. Ein natürlicher Engpass für den Handel.
#### Treibgut-Fallen
An einigen Stellen liegen große Steine oder umgestürtzte Bäume im Fluss. Sie bilden eine Gefahr für Boote, die hier oft hängenbleiben oder gar kentern.
Deshalb kann man an der ein oder anderen Stelle nützliche Gegenstände im Fluss finden.

## Events

> [!narrator] Auf dem Fluss 
> Das Wasser ist heute unruhig. Treibholz schießt schneller als gewöhnlich an euch vorbei, und der Pegel scheint in der letzten Stunde um eine Handbreit gestiegen zu sein. Irgendwo im Norden muss es stark geregnet haben – oder Schlimmeres.

Spült manchmal tote Fische an wegen Verseuchung.

## DM Wissen

Ein sehr langer Fluss quer durch die Dalelands. 
Die Lebensader der Region. 
Er fließt aus den Tiefen des [[Cormanthor]]-Waldes heraus. 
In letzter Zeit spült er manchmal tote, seltsam verformte Fische an.

Der Ashaba ist **nicht** für große Schiffe geeignet! 
**Schiffbarkeit:** Nur für Flöße, Kanus und Plattbodenboote (Kähne). Alles mit tiefem Kiel läuft auf Grund.
**Reiserichtung:** 
* *Flussabwärts (Süden):* Von [[Shadowdale]] über [[Ashabenford]] nach [[Essembra]] und Scardale. Schnell (Fast Pace), aber gefährlich wegen Felsen. 
* *Flussaufwärts (Norden):* Sehr mühsam. Meist werden Kähne von Pferden am Ufer getreidelt (gezogen).

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
