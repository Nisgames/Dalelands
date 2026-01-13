---
tags:
  - NPC
Status: Lebendig
Volk: Mensch
Klasse: Schläger
Level:
Ort: "[[Ashabenford]]"
Fraktionen: "[[Zhentarim]]"
Rolle: Höherer Schläger
Relevanz: Mittel
statblock: inline
---

## Erscheinung

*Klasse/Beruf:* `=this.Klasse` 
*Volk:* `=this.Volk` 
*Wohnort:* `=this.Ort` 
*Aussehen:* 
	Unglaublich breit gebaut und groß für einen Menschen.
	Muskulös und Hände wie ein Oger.
	Trägt eine hochwertige Lederrüstung mit schwarzen Nieten. 
	Sein Kopf ist kahlrasiert, bis auf einen Zopf am Hinterkopf
	Eine hässliche Brandnarbe zieht sich an seinem Hals hoch
*Charakterzug:* 
	Lässt lieber Taten als Worte sprechen.
	Relativ leicht reizbar.
*Sprechweise:* 
	Tief, langsam, gewählt. Trotz seines Auftretens handelt er meistens kühl.

## Werte & Loot:

> [!statblock]-
> 

> [!loot]- Loot
> 

## DM Wissen

- War dafür zuständig, die Kiste mit [[Schattensplitter]]n von [[Orin]] entegegen zu nehmen.

#### Begegnungen
```dataview
list without id link(file.link, title)
from #Session and !"00_Admin/03_Templates"
where contains(file.outlinks, this.file.link)
sort file.name asc
```
#### Plots
```dataview
table without id file.link as "Plot", category as "Kategorie"
from #Plot and !"00_Admin/03_Templates"
where contains(file.outlinks, this.file.link)
sort category asc
```
#### Items in Besitz
```dataview
list without id link(file.link, title)
from #Item and !"00_Admin/03_Templates"
where besitzer = this.file.link
sort file.name asc
```