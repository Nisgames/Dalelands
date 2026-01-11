---
tags:
  - NPC
Status: Lebendig
Volk: Drow
Klasse: Schurke
Level:
Ort: Underdark
Fraktionen: "[[Haus Jaelre]]"
Rolle: Handlanger
Relevanz: Mittel
statblock: inline
---

## Erscheinung

*Klasse/Beruf:* `=this.Klasse` 
*Volk:* `=this.Volk` 
*Wohnort:* `=this.Ort` 
*Aussehen:* 
- **Statur:** Drahtig und athletisch, bewegt sich mit einer fast unnatürlichen Flüssigkeit.
- **Kleidung:** Trägt funktionale, mattschwarze Lederkleidung, die kaum Geräusche macht. Ein dunkler Umhang hilft ihm, mit den Schatten zu verschmelzen.
- **Maskierung:** Sein Gesicht ist meist hinter einer stoffenen Maske oder einem hohen Kragen verborgen. Man sieht oft nur seine Augen, die im Dunkeln schwach rötlich schimmern (Darksight), oder das weiße Haar.
- **Ausrüstung:** Das [[Amulett der Zeit]] hängt offen um seinen Hals und pulsiert violett.
*Charakterzug:* 
- **Arrogant:** Betrachtet Oberflächenbewohner als "nutzlose Insekten".
- **Präzise:** Er verschwendet keine Worte und keine Bewegungen.
*Sprechweise:* 
- Seine Stimme ist ruhig, fast gelangweilt, selbst im Kampf.
- *Zitat:* "Eure Zeit ist abgelaufen, Affen."

## Werte & Loot:

[Link zum Statblock / (HP, AC) , Loot]

## DM Wissen

Ist ein Agent des [[Haus Jaelre]].
Wird oft für Außeneinsätze eingesetzt.

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