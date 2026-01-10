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
TABLE status FROM "10_Kampagne/12_Plots"
WHERE contains(beteiligte, this.file.link)
```

```dataview
list without id link(file.link, title)
from #Session where contains(file.outlinks, this.file.link)
sort file.name asc
```
