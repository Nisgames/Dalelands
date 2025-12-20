---
tags:
  - Player
Character: "[[Elina]]"
---
# Sessions

### Spieler
```dataview
TABLE
rows.PlayerCharacter AS "Gespielte Charaktere",
key.date AS "Datum"
FROM #session
FLATTEN Players AS PlayerCharacter
WHERE PlayerCharacter.Spieler = this.file.link
GROUP BY file.link AS "Session"
SORT key.date ASC
```

### DM
```dataview
TABLE WITHOUT ID
	file.link as Session,
	Players as Spieler,
	date as Datum
FROM #Session AND !"3-DM"
WHERE contains(DM, this.file.link)
SORT date ASC
```
