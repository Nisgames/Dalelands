---
tags:
  - NPC
Status: Lebendig
Volk: Mensch
Klasse: Schmied
Level:
Ort: "[[Ashabenford]]"
Fraktionen:
Rolle:
Relevanz: Niedrig
statblock: inline
---

## Erscheinung

*Klasse/Beruf:* `=this.Klasse` 
*Volk:* `=this.Volk` 
*Wohnort:* `=this.Ort` 
*Aussehen:* 
	Schlanke Frau mit gold-blondem Haar. Man sieht ihr ihren Job nicht an.
	Trägt meist eine Schmiede-Schürze
*Charakterzug:* 
	People-pleaser. Wenn man sie bittet, stellt sie fast alles für einen her.
*Sprechweise:* 
	[Langsam]

## Werte & Loot:

> [!statblock]-
> ![]

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