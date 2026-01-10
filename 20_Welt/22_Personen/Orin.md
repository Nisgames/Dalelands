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
- Ein Zettel mit einer verschlüsselten Notiz: *"Übergabe bei der alten Eiche entfällt. Bring es direkt zum Turm."*

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