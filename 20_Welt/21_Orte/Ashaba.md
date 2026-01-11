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

#### 1. Die Furt von [[Ashabenford]] 
Die bekannteste flache Stelle (siehe [[Ashabenford]]). Hier müssen Boote oft entladen oder über die Steine gezogen werden. Ein natürlicher Engpass für den Handel.

## Events

[Was passiert, wenn Bedingung X erfüllt ist?]

## DM Wissen

Ein sehr langer Fluss quer durch die Dalelands. 
Die Lebensader der Region. 
Er fließt aus den Tiefen des [[Cormanthor]]-Waldes heraus. 
In letzter Zeit spült er manchmal tote, seltsam verformte Fische an.

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
