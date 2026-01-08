---
tags:
  - Item
Magisch: false
Seltenheit:
Wert_in_GM:
Gewicht in KG:
Klassifikation:
Schaden:
Einstimmung: false
---
**Seltenheit:** `=this.Seltenheit` 
**Wert:** `=this.Wert_in_GM` GM
**Klassifikation:** `=this.Klassifikation` 
**Schaden:** `=this.Schaden`
**Beschreibung:** 

## 📰 Aktuelle Gerüchte & Plot-Hooks
```dataview
TABLE WITHOUT ID 
file.link AS "Plot",
regexreplace(Rows.text, "\[\[.*?\]\]", "") AS "Was passiert hier?"
FROM #Plot 
FLATTEN file.lists AS Rows
WHERE contains(Rows.outlinks, this.file.link) AND !file.frontmatter.resolved
```