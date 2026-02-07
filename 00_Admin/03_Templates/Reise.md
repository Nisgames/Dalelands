---
tags:
  - reise
Start: "[[Ort A]]"
Ziel: "[[Ort B]]"
Status: Aktiv
---
## Reise: `INPUT[Start]` nach `INPUT[Ziel]`

> [!abstract] Reise-Daten
> **START:** `VIEW[{Start}]`
> **ZIEL:** `VIEW[{Ziel}]`

---

## ETAPPE 1
> [!quote|no-icon] Übersicht
> **BEGINN:** > **ENDE:** > **STRECKE:** > **GELÄNDE:** > **WETTER:** | Tempo | Zeit (Tage/Stunden) |
| :--- | :--- |
| **SCHNELL** | |
| **NORMAL** | |
| **LANGSAM** | |

### ERZÄHLERISCHE NOTIZEN
- 

### HERAUSFORDERUNGEN
- 

**VERSTRICHENE ZEIT (GESAMT):** ---

## ETAPPE 2
> [!quote|no-icon] Übersicht
> **BEGINN:** > **ENDE:** > **STRECKE:** > **GELÄNDE:** > **WETTER:** | Tempo | Zeit (Tage/Stunden) |
| :--- | :--- |
| **SCHNELL** | |
| **NORMAL** | |
| **LANGSAM** | |

### ERZÄHLERISCHE NOTIZEN
- 

### HERAUSFORDERUNGEN
- 

**VERSTRICHENE ZEIT (GESAMT):** ```

### Erklärung der Änderungen
1.  **Properties (Frontmatter):** Oben zwischen den `---` stehen jetzt echte Metadaten. Wenn du das **Dataview** Plugin installiert hast, kannst du im Text statt `INPUT[...]` auch `` ` = this.Start ` `` schreiben, um es automatisch anzuzeigen.
2.  **Callouts:** Ich habe `> [!quote|no-icon]` verwendet. [cite_start]Im "fancy-a-story" Theme erzeugt das oft den gewünschten "Box"-Look[cite: 4], wie er im PDF um die Etappen-Details gezogen ist.
3.  [cite_start]**PDF-Felder:** Alle Felder wie *Beginn* [cite: 5][cite_start], *Ende* [cite: 6][cite_start], *Strecke* [cite: 9][cite_start], *Gelände* [cite: 10] [cite_start]und *Wetter* [cite: 13] sind jetzt als fester Text eingefügt, hinter den du einfach schreiben kannst.
4.  [cite_start]**Tabelle:** Die Geschwindigkeits-Tabelle [cite: 7, 11, 14] ist als reine Markdown-Tabelle formatiert, was sofort gerendert wird.

Funktioniert das optisch für dich im Theme?