---
tags:
  - NPC
name:
location: "[[ ]]"
faction: "[[ ]]"
status: alive
sex:
race:
---

**Rolle**:: 
**Ziel**:: 
**Stimme**:: 

## 📝 Beschreibung
* ## 🧠 Wissen & Secrets
- [ ] 

---
### 🔗 Kontext
*(Hier deine Dataview-Tabellen für Plot/Session)*
```dataview
TABLE WITHOUT ID file.link as "Plot", status
FROM "10_Kampagne/12_Plots"
WHERE contains(beteiligte, this.file.link)