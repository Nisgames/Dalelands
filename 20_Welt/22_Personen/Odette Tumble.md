---
tags:
  - NPC
Wohnort:
Klasse:
Volk: Mensch
Level:
Fraktionen:
Status: Lebendig
Relevanz: Niedrig
Ort:
Rolle:
statblock: inline
---

## Erscheinung

*Klasse/Beruf:* `=this.Klasse` 
*Volk:* `=this.Volk` 
*Wohnort:* `=this.Ort` 
*Aussehen:* Alte Frau (72), 157cm groß, langes rotbraunes Haar und hellbraune Augen
	Magerer Körperbau und eingefallene Haut
*Charakterzug:* Bleibt sehr ruhig und lässt sich nicht von Gefühlen leiten -> Muss gut handeln
*Sprechweise:* Reagiert immer mit einem "Haaa", gefolgt von einem wissenden Nicken

## Werte & Loot:

[Link zum Statblock / (HP, AC) , Loot]

## DM Wissen

[Motivation, Geheimnisse, Lügen]

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