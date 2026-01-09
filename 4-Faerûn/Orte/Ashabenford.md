---
tags:
  - Ort
Liegt_in: "[[Mistledale]]"
Fraktionen:
---

## 📖 Allgemeinwissen
Die Hauptstadt von **[[Mistledale]]**. 
Es ist ein offenes, geschäftiges Handelszentrum. 
Anders als manch andere Täler ist man hier friedlich und tolerant.

#### Glauben
In Ashabenford betet man pragmatisch:
- **Chauntea:** Für die Ernte (es ist ein Bauerntal).
- **Tymora:** Für das Glück im Handel.

### Hoher

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
