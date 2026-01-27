---
tags:
  - Ort
Region: "[[Cormanthor]]"
---

## Beschreibung

Der weiße Hain war einst ein offener Pavillon der Elfen 
Ein Ort der Kunst und Musik, bestehend aus weißen Marmorsäulen unter freiem Himmel

- Kreisrundes Plateau aus Marmor
- Umringt von uralten Eichen
	- Nicht herbstlich rot, sondern schneeweiß
- Offener Pavillon in der mitte von schlanken Säulen umringt
	- Teilweise von Efeu überwuchert, der violett schimmert
- In der Mitte des Pavillons steht eine Statue: Eine Elfe, die Harfe spielt
	- Kopf der Statue fehlt
	- An der Stelle wo das Herz wäre, pulsiert ein [[Schattensplitter]]
	- Er steckt tief im Marmor

## POI

#### Statue

Jeder, der sich der Statue auf 3 Meter nähert, muss einen **Weisheits-Rettungswurf (WIS Save DC 13)** machen.

-  **Bei Erfolg:** Der Charakter spürt die Trauer, kann aber handeln. Er kann versuchen, den Splitter mit einem **Stärke-Check (DC 14)** oder Werkzeugen ([[Jorvan]]) aus der Statue zu brechen.

-  **Bei Misserfolg ([[Bezaubert]]):** Der Charakter ist **[[Bezaubert]]** 
	- _Effekt:_ Er bleibt stehen, starrt den Splitter an und lächelt zufrieden. Er will den Splitter _beschützen_.
	- _Reaktion:_ Wenn ein anderer Spieler versucht, den Splitter zu nehmen, wird der bezauberte Charakter versuchen, ihn verbal ("Nein, er muss hier bleiben! Er ist so schön!") oder durch Festhalten (Grapple) zu stoppen. **Keine tödliche Gewalt**, nur Hindern.

## DM Wissen

Einst ein romantischer Ort der Kunst und Musik für die [[Myth Drannor Elfen]] 

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
