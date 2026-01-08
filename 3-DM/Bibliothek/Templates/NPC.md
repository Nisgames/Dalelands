---
tags:
  - NPC
Wohnort:
Klasse:
Volk:
Level:
Fraktionen:
Status: Lebendig
Relevanz:
---
# `=this.file.name`
*Klasse/Beruf:* `=this.Klasse` 
*Volk:* `=this.Volk` 
*Wohnort:* `=this.Wohnort` 
*Aussehen:* 
*Charakterzug:* 
*Sprechweise:* 

# Aussehen



# Beziehungen
- 

## 📰 Aktuelle Gerüchte & Plot-Hooks
```dataview
TABLE WITHOUT ID 
file.link AS "Plot",
regexreplace(Rows.text, "\[\[.*?\]\]", "") AS "Was passiert hier?"
FROM #Plot 
FLATTEN file.lists AS Rows
WHERE contains(Rows.outlinks, this.file.link) AND !file.frontmatter.resolved
```
