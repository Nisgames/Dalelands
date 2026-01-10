---
Aktueller-Ort: "[[Ashabenford]]"
---

# 🛡️ DnD Wächter der Dalelands

### ☑️ To-Do´s
- [ ] Session 1 vorbereiten
---

### 🧭 Schnellzugriff

👥 Alle Charaktere: [[Charaktere \|CHARAKTER-ÜBERSICHT]]       
### Offene Quests

```dataview
List
FROM #Quest AND !"3-DM/Bibliothek/Templates"
WHERE !Erledigt
GROUP BY file.link
```

### Wichtige NPC

```dataview
TABLE
  status AS "Status"
FROM #NPC  
WHERE contains(["Hoch", "Sehr hoch", "Elementar"], Relevanz) AND Status = "Lebendig"
SORT file.name ASC
```

### Historie

```dataview
TABLE
  date AS "Datum",
  join(Players.Spieler, ", ") AS "Teilnehmer"
FROM #session
WHERE date != null
SORT date DESC
LIMIT 10
```

---

### 👥 Spielercharaktere

```dataview
TABLE WITHOUT ID
  file.link as Charakter,
  Spieler AS "Gespielt von",
  volk AS "Volk",
  klasse AS "Klasse"
FROM #PC 
WHERE Spieler != null
SORT file.name ASC
```
