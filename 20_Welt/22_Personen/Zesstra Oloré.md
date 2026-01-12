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
*Aussehen:* [Klein mit Bart]
*Charakterzug:* [Hasst Wein]
*Sprechweise:* [Langsam]

## Werte & Loot:

> [!statblock]-
> 

> [!loot]- Loot
> 

## DM Wissen

- **Beziehung zu [[Valzoun]]:** Sie verachtet ihn als männlichen Magier und Nicht-Drow, braucht aber sein technisches Wissen. Sobald der Monolith funktioniert, plant sie, ihn zu entsorgen. 
- **Aufenthaltsort:** Sie bewegt sich meist im tiefen **[[Cormanthor]]**, taucht aber auf, wenn Untergebene (wie [[Varon]]) versagen, um "aufzuräumen".

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