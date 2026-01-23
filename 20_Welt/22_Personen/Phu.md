---
tags:
  - NPC
Status: Lebendig
Volk: Bär
Klasse:
Level:
Ort: "[[Elina]]"
Fraktionen: "[[Spieler Party]]"
Rolle:
Relevanz: Hoch
statblock: inline
---

## Erscheinung

*Klasse/Beruf:* `=this.Klasse` 
*Volk:* `=this.Volk` 
*Wohnort:* `=this.Ort` 
*Aussehen:* 
	Ein müstisch aussehender Bär.

## Werte & Loot:

> [!statblock]-
> ![[Statblock_Phu]]

> [!loot]- Loot
> 

## DM Wissen

Urtier des Landes von [[Elina]] als Waldläufer Herrin der Tiere.

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