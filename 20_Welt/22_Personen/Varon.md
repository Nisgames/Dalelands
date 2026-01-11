---
tags:
  - NPC
Status: Lebendig
Volk: Drow
Klasse:
Level:
Ort:
Fraktionen: "[[Haus Jaelre]]"
Rolle: Handlanger
Relevanz: Mittel
statblock: inline
---

## Erscheinung

*Klasse/Beruf:* `=this.Klasse` 
*Volk:* `=this.Volk` 
*Wohnort:* `=this.Ort` 
*Aussehen:* [Klein mit Bart]
*Charakterzug:* [Hasst Wein]
*Sprechweise:* [Langsam]

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