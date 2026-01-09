
### Was müssen die Spieler wissen?

```dataview
TABLE without id
	link(file.path, regexreplace(file.name, "^Wissen - ", "")) as Thema,
	INT as "Ab INT"
from #Allgemeinwissen and !"3-DM/Bibliothek/Templates"
sort file.name ASC
```
