---
Start: Ort A
Ziel: Ort B
Status: Reise läuft
tags:
  - reise
---
# Reise: `= this.Start` nach `= this.Ziel`

> [!info] Reise-Daten
> **START:** `= this.Start`
> **ZIEL:** `= this.Ziel`

---

## ETAPPE 1

> [!quote] Logistik
> **BEGINN:** > **ENDE:** > **STRECKE:** > **GELÄNDE:** > **WETTER:** >
> | Tempo | Zeit (Tage/Stunden) |
> | :--- | :--- |
> | **SCHNELL** | |
> | **NORMAL** | |
> | **LANGSAM** | |

### ERZÄHLERISCHE NOTIZEN
- 

### HERAUSFORDERUNGEN
- 

**VERSTRICHENE ZEIT (TAGE/STD.):** ---

## ETAPPE 2

> [!quote] Logistik
> **BEGINN:** > **ENDE:** > **STRECKE:** > **GELÄNDE:** > **WETTER:** >
> | Tempo | Zeit (Tage/Stunden) |
> | :--- | :--- |
> | **SCHNELL** | |
> | **NORMAL** | |
> | **LANGSAM** | |

### ERZÄHLERISCHE NOTIZEN
- 

### HERAUSFORDERUNGEN
- 

**VERSTRICHENE ZEIT (TAGE/STD.):** ---

## ZUSAMMENFASSUNG
**GESAMTZEIT:** ```

### Warum es jetzt funktioniert:
1.  **Die leere `>` Zeile:** Vor der Tabelle (`| Tempo |...`) ist jetzt eine Zeile, die nur ein `>` enthält. Das signalisiert Obsidian: "Hier endet der Text, jetzt kommt ein neues Element (die Tabelle)."
2.  **Zeilenumbrüche:** *Beginn*, *Ende*, *Strecke* stehen jetzt untereinander. Das ist stabiler als alles in eine Zeile zu quetschen und sieht in der Box auch aufgeräumter aus.