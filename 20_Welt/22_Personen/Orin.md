---
tags:
  - NPC
Status: Lebendig
Volk: Mensch
Klasse: Schmuggler
Level:
Ort: "[[Ashabenford]]"
Fraktionen: "[[Zhentarim]]"
Rolle: Handlanger
Relevanz: Mittel
---

## Erscheinung

*Klasse/Beruf:* `=this.Klasse` 
*Volk:* `=this.Volk` 
*Wohnort:* `=this.Ort` 
*Aussehen:* 
	Trägt gut geschnittene, dunkle Reisekleidung. 
	Er hat glattes, öliges schwarzes Haar und ein blasses Gesicht. 
	Seine Augen scannen ständig den Raum.
*Charakterzug:* Leicht reizbar
*Sprechweise:* Hastig, verschluckt oft Wortenden. 
	Wenn er sich sicher fühlt (oder [[Zhentarim]] im Rücken hat), wird er arrogant.

## Werte & Loot:

**Loot:** 
- Ein Briefsiegel der Zhentarim (versteckt in einer hohlen Absatzsohle). 
- 15 GM in verschiedenen Währungen (Sembia, Cormyr).

## DM Wissen

**Hintergrund:** Orin ist ein niederrangiger Kurier der [[Zhentarim]], der hofft, durch diese wichtige Lieferung aufzusteigen. Er weiß nicht genau, *was* in der Kiste ist, nur dass es extrem wertvoll und magisch ist. Die Kiste wurde ihm in Hillsfar übergeben. 

**Motivation:** Er hat massive Spielschulden und die Zhentarim haben ihm "eine letzte Chance" gegeben. Wenn er die Kiste verliert, ist er so gut wie tot. Deshalb seine extreme Panik im Gasthaus.

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