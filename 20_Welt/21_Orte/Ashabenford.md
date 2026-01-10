---
tags:
  - Ort
  - Stadt
Region: [[Mistledale]]
---

## Sinneswahrnehmung

[Was hören, sehen, riechen beim Betreten?]

- *Sehen:* 
- *Beleuchtung:* 
- *Hören:* 
- *Riechen:* 
- *Spüren:* 
- *Atmosphäre:* 
- *Details:* 

## POI

#### Glauben
In Ashabenford betet man pragmatisch:
- **Chauntea:** Für die Ernte (es ist ein Bauerntal).
- **Tymora:** Für das Glück im Handel.

#### Hoher Rat
[[Ashabenford]] wird von einem Rat regiert ([[Bürgermeisterin Andra]]). 
Sie suchen händeringend nach Söldnern, um die Straßen sicher zu halten.

## Events

[Was passiert, wenn Bedingung X erfüllt ist?]

## DM Wissen

Die Hauptstadt von **[[Mistledale]]**. 
Es ist ein offenes, geschäftiges Handelszentrum. 
Anders als manch andere Täler ist man hier friedlich und tolerant.

#### Bewohner
```dataview
table without id file.link as Name
from #NPC and !"00_Admin/03_Templates"
where contains(Ort, this.file.link) 
	and status != "Tot"
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
