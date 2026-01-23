---
tags:
  - NPC
Status: Lebendig
Volk: Mensch
Klasse: Kämpfer
Level: 3
Ort: "[[Cormanthor]]"
Fraktionen: "[[Zhentarim]]"
Rolle: Neuling
Relevanz: Niedrig
statblock: inline
---

## Erscheinung

*Klasse/Beruf:* `=this.Klasse` 
*Volk:* `=this.Volk` 
*Wohnort:* `=this.Ort` 
*Aussehen:* 
	Klein, blond, etwa 20 Jahre alt
	Wirkt sehr energetisch
*Charakterzug:* 
	Neu bei den [[Zhentarim]] und sehr engagiert
*Sprechweise:* 
	Sehr höflich und zuvorkommend

## Werte & Loot:

> [!statblock]-
> ![[Statblock_Tom_Flinken]]

> [!loot]- Loot
> 

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