---
tags:
  - NPC
Status: Lebendig
Volk: Ork
Klasse: Paladin
Level:
Ort: "[[Rashemen]]"
Fraktionen:
Rolle:
Relevanz: Mittel
statblock: inline
---

## Erscheinung

*Klasse/Beruf:* `=this.Klasse` 
*Volk:* `=this.Volk` 
*Wohnort:* `=this.Ort` 
*Aussehen:* 
	[Klein mit Bart]
*Charakterzug:* 
	[Hasst Wein]
*Sprechweise:* 
	[Langsam]

## Werte & Loot:

> [!statblock]-
> ![]

> [!loot]- Loot
> 

## DM Wissen

Ork Kleriker [[Lathander]].
Kindheitsfreund von [[Tado]].
Als [[Tado]] seinen Pakt mit [[Tados Patron]] geschlossen hat, hat auch [[Zeek Reißzahn]] einen Pakt mit [[Tados Patron]] geschlossen.
Auch er hat das Bewusstsein verloren und ist in den [[Dalelands]] aufgewacht.

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