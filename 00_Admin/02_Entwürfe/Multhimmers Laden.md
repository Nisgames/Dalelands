---
tags:
  - Ort
Region:
---

## Beschreibung

Handelshaus in [[Ashabenford]]. Ist bekannt dafür, _alles_ zu kaufen und zu verkaufen.

- Ein großes, chaotisches Gebäude. Sieht aus als wäre mehrfach angebaut worden.
- **Innen**: Ein Labyrinth aus Gängen voller Regale. Nicht wirklich sortiert.
	- Es riecht nach Pökelfleisch, Wolle und Lampenöl
	- Beluchtung ist spärlich, was das Suchen noch erschwert

## POI

#### Regale

- Gefüllt mit jeglichen Dingen: Lebensmittel, Stoffe, Abenteurerausrüstungen (Fackeln, Seile, etc)

#### Theke



## DM Wissen

Der Laden wird geführt von [[Multhimmer]].

#### Bewohner
```dataview
table without id file.link as Name
from #NPC and !"00_Admin/03_Templates"
where contains(Ort, this.file.link) 
	and status != "Tot"
sort file.name asc
```
#### Historie
```dataview
list without id link(file.link, title)
from #Session and !"00_Admin/03_Templates"
where contains(file.outlinks, this.file.link)
```
#### Plot Events
```dataview
task 
from #Plot and !"00_Admin/03_Templates"
where contains(tags, "#loc/" + this.file.name)
	and !resolved
```
