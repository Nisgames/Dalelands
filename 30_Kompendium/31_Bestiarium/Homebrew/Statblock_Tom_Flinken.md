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
hp: 28
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
languages: Gemeinsprache
cr: 1
traits:
  - name: "Waffenmeisterschaft: Streifen (Zweihänder)"
    desc: "Wenn Tom mit dem Zweihänder verfehlt, erleidet das Ziel dennoch Schaden in Höhe seines Stärke-Modifikators (4 Schaden)."
  - name: "Waffenmeisterschaft: Irritieren (Handaxt)"
    desc: "Wenn Tom mit der Handaxt trifft und Schaden verursacht, hat er Vorteil (Advantage) auf den nächsten Angriffswurf gegen dieses Ziel vor Ende seines nächsten Zuges."
  - name: "Kampfstil: Kampf mit großen Waffen"
    desc: "Wenn Tom beim Schaden für eine zweihändige Waffe eine 1 oder 2 würfelt, wird das Ergebnis als 3 behandelt."
  - name: "Talent: Brutaler Angreifer"
    desc: "Einmal pro Zug, wenn Tom mit einer Waffe trifft, kann er den Waffenschaden zweimal würfeln und das höhere Ergebnis verwenden."
  - name: "Kampfüberlegenheit (4/Kurze Rast)"
    desc: "Tom hat **4 W8**. Er nutzt diese für Manöver. SG für Rettungswürfe ist 14."
  - name: "Magischer Gegenstand: Ogerkraft-Handschuhe"
    desc: "Stärke ist magisch auf 19 gesetzt."
actions:
  - name: "Zweihänder"
    desc: "Nahkampf: +6 zum Treffen, Reichweite 1,5 m. Treffer: 11 (2d6 + 4) Hiebschaden. (Dank Kampfstil ist der Minimalschaden bei einem Treffer immer 10)."
  - name: "Handaxt"
    desc: "Nahkampf/Fernkampf: +6 zum Treffen, Reichweite 6/18 m. Treffer: 7 (1d6 + 4) Hiebschaden."
  - name: "Tatendrang (1/Rast)"
    desc: "Tom führt eine zusätzliche Aktion in seinem Zug aus."
  - name: "Manöver: Präzisionsangriff"
    desc: "Verbrauche 1 W8 und addiere das Ergebnis zum Angriffswurf."
  - name: "Manöver: Zu Fall bringen"
    desc: "Verbrauche 1 W8. Bei Treffer: +1d8 Schaden. Ziel muss STR-Rettungswurf (SG 14) bestehen oder ist liegend."
bonus_actions:
  - name: "Durchschnaufen (2/Rast)"
    desc: "Heilt 1d10 + 3 TP. Kann dank 'Taktischer Verstand' verbraucht werden, um 1d10 auf einen gescheiterten Fähigkeitswurf zu addieren."
reactions:
  - name: "Manöver: Riposte"
    desc: "Wenn ein Gegner verfehlt: Verbrauche 1 W8 für sofortigen Gegenangriff (+1d8 Schaden)."
```
