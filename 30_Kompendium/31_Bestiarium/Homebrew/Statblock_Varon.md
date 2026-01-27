---
tags:
  - Monster
sourcebook: Homebrew
CR: "2"
statblock: inline
---

```statblock
name: Varon
size: Mittelgroß
type: Elf
subtype: Drow
source: Homebrew
alignment: Neutral Böse
ac: 15 (Beschlagenes Leder)
hp: 44
hit_dice: 8d8 + 8
speed: 30 Fuß
stats: [11, 18, 12, 13, 12, 13]
saves:
  - Dex: +6
skillsaves:
  - Heimlichkeit: +6
  - Akrobatik: +6
  - Wahrnehmung: +3
senses: Dunkelsicht 120 Fuß, passive Wahrnehmung 13
languages: [[Elfisch]], [[Untergemeinsprache]], [[Gemeinsprache]]
cr: 2
traits:
  - name: Feenblut
    desc: "Varon ist im Vorteil bei Rettungswürfen gegen den Zustand Bezaubert, und Magie kann ihn nicht einschläfern."
  - name: Empfindlichkeit gegen Sonnenlicht
    desc: "Im Sonnenlicht ist Varon bei Angriffswürfen sowie bei Weisheitswürfen (Wahrnehmung), die auf Sicht basieren, im Nachteil."
  - name: Angeborenes Zauberwirken (Drow)
    desc: "Varons Attribut zum Zauberwirken ist Charisma (SG 11 für Rettungswürfe gegen Zauber). Er kann von Natur aus die folgenden Zauber wirken, ohne Materialkomponenten zu benötigen:\n1/Tag jeweils: Dunkelheit, Feenfeuer"
  - name: Nebel-Schritt (3/Tag)
    desc: "Als Bonusaktion kann Varon *Nebeltritt* (Misty Step) wirken (Teleportation 30 Fuß). Dabei hinterlässt er ein violettes Nachbild, das sofort verblasst."
actions:
  - name: Mehrfachangriff
    desc: "Varon führt zwei Angriffe mit seinem Kurzschwert oder seiner Handarmbrust aus."
  - name: Kurzschwert
    desc: "Nahkampf-Waffenangriff: +6 zum Treffen, Reichweite 5 Fuß, ein Ziel. Treffer: 7 (1d6 + 4) Stichschaden plus 3 (1d6) Giftschaden."
  - name: Handarmbrust
    desc: "Fernkampf-Waffenangriff: +6 zum Treffen, Reichweite 30/120 Fuß, ein Ziel. Treffer: 7 (1d6 + 4) Stichschaden."
bonus_actions:
  - name: Listige Aktion
    desc: "Varon kann in jedem seiner Züge die Aktion Sputen, Rückzug oder Verstecken als Bonusaktion nehmen."
```

```dataview
name: Drow-Elitekrieger
size: Mittelgroß
type: Humanoider (Elf)
alignment: neutral böse
ac: 18
armor_desc: beschlagene Lederrüstung, Schild
hp: 71
hit_dice: 11w8 + 22
speed: 9 m
stats: [13, 18, 14, 11, 13, 12]
saves:
  - dexterity: 7
  - constitution: 5
  - wisdom: 4
skills:
  - Heimlichkeit: 10
  - Wahrnehmung: 4
senses: Dunkelsicht 36 m, passive Wahrnehmung 14
languages: Elfisch, Gemeinsprache der Unterreiche
cr: 5
traits:
  - name: Feenblut
    desc: "Der Drow hat einen Vorteil bei Rettungswürfen, wenn er bezaubert werden soll, und Magie kann ihn nicht einschläfern."
  - name: Angeborenes Zauberwirken
    desc: "Das Attribut zum Wirken angeborener Zauber für den Drow ist Charisma (Zauberrettungswurf-SG 12). Der Drow kann angeboren die folgenden Zauber wirken, wobei keine Materialkomponenten nötig sind:\n\n* **Willentlich:** Tanzende Lichter\n* **Jeweils 1/Tag:** Dunkelheit, Feenfeuer, Schweben (nur selbst)"
  - name: Empfindlich gegenüber Sonnenlicht
    desc: "Solange sich der Drow im Sonnenlicht befindet, erleidet er einen Nachteil auf Angriffswürfe, sowie auf Würfe mit Weisheit (Wahrnehmung), die auf Sicht beruhen."
actions:
  - name: Mehrfachangriff
    desc: "Der Drow führt zwei Kurzschwert-Angriffe aus."
  - name: Kurzschwert
    desc: "Nahkampf-Waffenangriff: +7 zum Treffen, Reichweite 1,5 m, ein Ziel. Treffer: 7 (1W6 + 4) Stichschaden plus 10 (3W6) Giftschaden."
  - name: Handarmbrust
    desc: "Fernkampf-Waffenangriff: +7 zum Treffen, Reichweite 9/36 m, ein Ziel. Treffer: 7 (1W6 + 4) Stichschaden, und das Ziel muss einen Konstitutionsrettungswurf gegen SG 13 ablegen, um nicht für 1 Stunde vergiftet zu werden. Wenn der Rettungswurf um 5 oder mehr Punkte misslingt, wird das Ziel auch bewusstlos, solange es auf diese Weise vergiftet ist. Das Ziel erwacht, wenn es Schaden erleidet oder eine andere Kreatur eine Aktion ausführt, um es wachzurütteln."
reactions:
  - name: Parade
    desc: "Der Drow addiert 3 auf seine RK gegen einen Nahkampfangriff, der ihn treffen würde. Dazu muss der Drow den Angreifer sehen und eine Nahkampfwaffe führen."

```