---
tags:
  - Monster
sourcebook: Homebrew
CR:
statblock: inline
---

```statblock
name: Tom Flinken
size: Mittelgroß
type: Humanoid (Mensch)
alignment: Neutral
ac: 16 (Kettenpanzer)
hp: 28 (3d10 + 9)
hit_dice: 3d10
speed: 9 m
stats: [19, 14, 16, 10, 12, 8]
saves:
  - Stärke: +6
  - Konstitution: +5
skillsaves:
  - Athletik: +6
  - Wahrnehmung: +3
  - Überleben: +3
senses: Passive Wahrnehmung 13
languages: [[Gemeinsprache]]
cr: 1
traits:
  - name: "Magischer Gegenstand: [[Panzerhandschuhe der Ogerkraft]]"
    desc: "Toms Stärke wird auf 19 gesetzt (bereits eingerechnet). Er erhält dadurch +4 auf Stärke-Checks und Angriffe."
  - name: "Kampfstil: Kampf mit großen Waffen"
    desc: "Bei einer 1 oder 2 auf dem Schadenswürfel (Zweihänder) darf der Würfel einmal neu geworfen werden."
  - name: "Tatendrang (1/Rast)"
    desc: "Tom kann eine zusätzliche Standardaktion in seinem Zug ausführen."
  - name: "Talent: Meister der großen Waffen"
    desc: "Bei Krit oder Kill: Ein Nahkampfangriff als Bonusaktion.<br>Optional: -5 auf Angriff für +10 Schaden."
actions:
  - name: "Zweihänder"
    desc: "Nahkampf-Waffenangriff: +6 zum Treffen, Reichweite 1,5 m, ein Ziel. Treffer: 11 (2d6 + 4) Hiebschaden."
  - name: "Handaxt"
    desc: "Nahkampf- oder Fernkampfangriff: +6 zum Treffen, Reichweite 6/18 m, ein Ziel. Treffer: 7 (1d6 + 4) Hiebschaden."
  - name: "Manöver: Präzisionsangriff"
    desc: "Kann einen Überlegenheitswürfel (d8) zum Angriffswurf addieren (vor oder nach dem Wurf)."
  - name: "Manöver: Zu Fall bringen"
    desc: "Bei Treffer: +1d8 Schaden. Ziel muss STR-Rettungswurf (SG 14) bestehen oder ist liegend."
bonus_actions:
  - name: "Durchschnaufen (1/Rast)"
    desc: "Heilt 1d10 + 3 Trefferpunkte."
reactions:
  - name: "Manöver: Riposte"
    desc: "Wenn ein Gegner Tom im Nahkampf verfehlt, kann er seine Reaktion nutzen, um einen Angriff gegen diese Kreatur auszuführen (+1d8 Schaden bei Treffer)."
```
