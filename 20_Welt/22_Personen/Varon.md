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

> [!statblock]- Statblock
> ```statblock
> name: Varon (Drow)
> size: Mittelgroß
> type: Humanoider
> subtype: Elf
> alignment: Neutral Böse
> ac: 15
> hp: 44
> hit_dice: 8d8 + 8
> speed: 30 Fuß
> stats: [11, 18, 12, 13, 12, 13]
> saves:
>   - Dex: +6
> skillsaves:
>   - Heimlichkeit: +6
>   - Akrobatik: +6
>   - Wahrnehmung: +3
> senses: Dunkelsicht 120 Fuß, passive Wahrnehmung 13
> languages: Elfisch, Untergemeinsprache, Gemeinsprache
> cr: 2
> traits:
>   - name: Feenblut
>     desc: "Varon ist im Vorteil bei Rettungswürfen gegen den Zustand Bezaubert, und Magie kann ihn nicht einschläfern."
>   - name: Empfindlichkeit gegen Sonnenlicht
>     desc: "Im Sonnenlicht ist Varon bei Angriffswürfen sowie bei Weisheitswürfen (Wahrnehmung), die auf Sicht basieren, im Nachteil."
>   - name: Angeborenes Zauberwirken (Drow)
>     desc: "Varons Attribut zum Zauberwirken ist Charisma (SG 11 für Rettungswürfe gegen Zauber). Er kann von Natur aus die folgenden Zauber wirken, ohne Materialkomponenten zu benötigen:\n1/Tag jeweils: Dunkelheit, Feenfeuer"
>   - name: Amulett-Schritt (3/Tag)
>     desc: "Als Bonusaktion kann Varon die Macht des Amuletts nutzen, um *Nebeltritt* (Misty Step) zu wirken (Teleportation 30 Fuß). Dabei hinterlässt er ein violettes Nachbild, das sofort verblasst."
> actions:
>   - name: Mehrfachangriff
>     desc: "Varon führt zwei Angriffe mit seinem Kurzschwert oder seiner Handarmbrust aus."
>   - name: Kurzschwert
>     desc: "Nahkampf-Waffenangriff: +6 zum Treffen, Reichweite 5 Fuß, ein Ziel. Treffer: 7 (1d6 + 4) Stichschaden plus 3 (1d6) Giftschaden."
>   - name: Handarmbrust
>     desc: "Fernkampf-Waffenangriff: +6 zum Treffen, Reichweite 30/120 Fuß, ein Ziel. Treffer: 7 (1d6 + 4) Stichschaden."
> bonus_actions:
>   - name: Listige Aktion
>     desc: "Varon kann in jedem seiner Züge die Aktion Sputen, Rückzug oder Verstecken als Bonusaktion nehmen."
> ```


> [!loot]- Loot
> 


## DM Wissen

Ist ein Agent des [[Haus Jaelre]].
Wird oft für Außeneinsätze eingesetzt.
Kämpft dreckig - nimmt auch gerne mal Geiseln

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