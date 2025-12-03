
### Was müssen die Spieler wissen?
- Wir befinden uns 1496DR
- Zerstörung von Myth Drannor (Hauptstadt des Elfenterritoriums) 1487

```dataview
TABLE without id
	link(file.path, regexreplace(file.name, "^Wissen - ", "")) as Thema,
	INT as "Ab INT"
from #Allgemeinwissen and !"3-DM/Bibliothek/Templates"
```
