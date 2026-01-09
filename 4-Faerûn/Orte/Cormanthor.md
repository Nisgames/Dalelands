---
tags:
  - Ort
Liegt_in: "[[Dalelands]]"
Fraktionen:
---

## 📖 Allgemeinwissen

- **Die Grüne Hölle:** Der gigantische Wald, der die Täler umgibt. Früher die Heimat der Elfen, heute ein gefährliches Niemandsland.
    
- **Die Regel:** "Bleib auf den Wegen." Wer tief ins Dickicht geht, kommt selten zurück. Es heißt, seit dem Absturz seien die Tiere aggressiver geworden.
    
- **Die Drow:** Es ist ein offenes Geheimnis, dass Dunkelelfen (Drow) die Schatten des Waldes nutzen, um Überfälle zu begehen. Man fürchtet sie, sieht sie aber selten.

## 📰 Aktuelle Gerüchte & Plot-Hooks
```dataview
TABLE WITHOUT ID 
file.link AS "Plot",
regexreplace(Rows.text, "\[\[.*?\]\]", "") AS "Was passiert hier?"
FROM #Plot 
FLATTEN file.lists AS Rows
WHERE contains(Rows.outlinks, this.file.link) AND !file.frontmatter.resolved
```

## Bewohner
```dataview
TABLE WITHOUT ID
	file.link as Name,
	Relevanz as Relevanz
from #NPC AND !"3-DM/"
where contains(Wohnort, this.file.link)
```
