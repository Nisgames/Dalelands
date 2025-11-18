
---

```dataview
TABLE WITHOUT ID
	file.link as Session,
	date as Datum,
	Players as Spieler,
	DM as DM
FROM #Session AND !"3-DM"
SORT date ASC
```
