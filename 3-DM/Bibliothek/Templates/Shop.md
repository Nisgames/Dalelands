---
tags:
  - Ort
  - Shop
Liegt_in:
Fraktionen:
---
---

# **`=this.file.name`**

### Beschreibung

### Besitzer

### Angebot
| Item | Beschreibung | Preis |
| ---- | ------------ | ----- |
|      |              |       |
|      |              |       |
|      |              |       |
### Details

---
## 📰 Aktuelle Gerüchte & Plot-Hooks
```dataview
TABLE WITHOUT ID 
file.link AS "Plot",
regexreplace(Rows.text, "\[\[.*?\]\]", "") AS "Was passiert hier?"
FROM #Plot 
FLATTEN file.lists AS Rows
WHERE contains(Rows.outlinks, this.file.link) AND !file.frontmatter.resolved
```

