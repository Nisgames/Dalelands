---
Aktueller-Ort: "[[Ashabenford]]"
---

# 🛡️ DnD Wächter der Dalelands

## ☑️ To-Do´s

```dataview
task
from #Session 
where !completed  
GROUP BY file.link
```

---

## 🧭 Schnellzugriff

👥 Alle Charaktere: [[Charaktere \|CHARAKTER-ÜBERSICHT]] 

Session Bewertungen: [Bewertungen](https://docs.google.com/spreadsheets/d/1lrYEuFlWl42Ezlp9MG29IAiasV_SwR5LY9N6ni8Z-6w/edit?gid=1104407416#gid=1104407416)

Letzte Session: `$= dv.pages("#Session").where(p => p.date < dv.date('today')).sort(p => p.date, 'desc').first().file.link` 

Nächste Session: `$= dv.pages("#Session").where(p => p.date >= dv.date('today')).sort(p => p.date, 'asc').first().file.link`

#### Offene Plots
```dataview
List
FROM #Plot AND !"00_Admin/03_Templates"
WHERE !resolved
sort file.name
```

#### Wichtige NPC
```dataview
TABLE without id
	file.link as "Name",
	relevanz as "Relevanz",
	status AS "Status"
FROM #NPC and !"00_Admin/03_Templates"
WHERE contains(["Hoch", "Sehr hoch", "Elementar"], Relevanz) AND Status = "Lebendig"
SORT relevanz, file.name ASC
```

#### Historie
```dataview
TABLE
  date AS "Datum"
FROM #Session 
WHERE date != null
SORT date DESC
LIMIT 10
```

#### Spielercharaktere
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
