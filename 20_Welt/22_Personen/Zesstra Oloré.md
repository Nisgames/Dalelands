---
tags:
  - NPC
Status: Lebendig
Volk: Drow
Klasse: Priesterin der Lolth
Level:
Ort: Underdark
Fraktionen: "[[Haus Jaelre]]"
Rolle: Feldkommandantin
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
	Eiskalt, effizient und humorlos. Im Gegensatz zu vielen chaotischen Drow schätzt sie militärische Disziplin. Versagen bestraft sie nicht mit Wut, sondern mit tödlicher Präzision.
*Sprechweise:* 
	[Langsam]
*Rolle:* 
	Feldkommandantin und Priesterin der Lolth für die Oberflächen-Operationen von [[Haus Jaelre]].

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