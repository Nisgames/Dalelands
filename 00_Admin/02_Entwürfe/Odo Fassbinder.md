---
tags:
  - NPC
Status: Lebendig
Volk:
Klasse:
Level:
Ort:
Fraktionen:
Rolle:
Relevanz:
statblock: inline
---

## Erscheinung

*Klasse/Beruf:* `=this.Klasse` 
*Volk:* `=this.Volk` 
*Wohnort:* `=this.Ort` 
*Aussehen:* 
	Ein korpulenter Halbling mit rosigen Wangen und einer fast religiösen Hingabe zu Milchprodukten.
*Charakterzug:* 
	Er ist hektisch, laut, aber gutherzig.
*Sprechweise:* 
	[Langsam]
*Rolle:*
	Käsemeister von [[Ashabenford]].
*Motivation:*
	Will den "Nebeltaler Stinkekäse" beim jährlichen Wettbewerb präsentieren und seinen Rivalen aus [[Mistledale]] schlagen.

**Sprache/Verhalten:**
* Nutzt viele kulinarische Metaphern ("Das ist doch Käse!", "Alles in Butter").
* Fasst sich oft theatralisch an die Brust.
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