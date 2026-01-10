---
tags:
  - NPC
Status: Lebendig
Volk:
Klasse:
Level:
Ort:
Fraktionen:
Relevanz:
---

## Erscheinung

*Klasse/Beruf:* `=this.Klasse` 
*Volk:* `=this.Volk` 
*Wohnort:* `=this.Ort` 
*Aussehen:* 
*Charakterzug:* 
*Sprechweise:* 

## Werte & Loot:

[Link zum Statblock / (HP, AC) , Loot]

## DM Wissen

[Motivation, Geheimnisse, Lügen]

### Begegnungen
```dataview
list without id link(file.link, title)
from #Session and !"00_Admin/03_Templates"
where contains(file.outlinks, this.file.link)
sort file.name asc
```
### Plots
```dataview
table without id file.links as "Plot", status
from #Plot and !"00_Admin/03_Templates"
where contains(file.outlinks, this.file.link)
```
