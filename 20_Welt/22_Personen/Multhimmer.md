---
tags:
  - NPC
Status: Lebendig
Volk: Mensch
Klasse: Schurke / Ladenbesitzer
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
	Mittelalt, strubbeliger Bart
	Braune Haare, wache Augen
*Charakterzug:* 
	Scheut sich nicht, Reisende übers Ohr zu hauen
*Sprechweise:* 
	Kalt und bedacht

## Werte & Loot:

> [!statblock]-
> ![]

> [!loot]- Loot
> 

## DM Wissen

Verkauft in [[Multhimmers Laden]] Gegenstände für 20% über dem Marktpreis

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