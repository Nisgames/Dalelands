---
tags:
  - NPC
Status: Lebendig
Volk: Mensch
Klasse: Kämpfer
Level: 3
Ort: "[[Cormanthor]]"
Fraktionen: "[[Zhentarim]]"
Rolle: Reißzahn
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
	Muskulös gebaut, sieht nicht schwach aus
	Trägt stolz ein gelbes [[Zhentarim]] Cape und eine Anstecknadel an seinem Kettenpanzer
*Charakterzug:* 
	Neu bei den [[Zhentarim]] und sehr engagiert. Denkt, er arbeitet für die Guten.
	Ist sehr mutig und aufgeschlossen
*Sprechweise:* 
	Sehr höflich und zuvorkommend

## Werte & Loot:

> [!statblock]-
> ![[Statblock_Tom_Flinken]]

> [!loot]- Loot
> 

## DM Wissen

Ist aufgewachsen in [[Daggerdale]].
![[Daggerdale#Zhentarim]]

Er hat sich die [[Zhentarim]] als Vorbild genommen und will genau wie sie das Tal beschützen.

Anfang Marpenoth 1496 wurde er als Fernspäher entsandt, um die Drow Aktivitäten von [[Haus Jaelre]] in [[Cormanthor]] zu beobachten und zu berichten. Seitdem lebt er im Wald, schläft im Dreck und isst Eichhörnchen.

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