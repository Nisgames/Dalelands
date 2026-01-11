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

![[Pasted image 20260111153525.png]]

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

#### 1. Architektur & Stadtbild: Rustikal & Nebel-tauglich

Ashabenford ist keine steinerne Festung wie Waterdeep, sondern eine gewachsene, ländliche Handelsstadt.

- **Keine Brücke, sondern eine Furt!** Der Name "Ashabenford" kommt von der flachen Stelle im Fluss Ashaba. Es gibt hier **keine große Steinbrücke**.
    
    - _Beschreibung:_ Beschreibe, wie Karren durch das knietiefe, kalte Wasser rumpeln oder über rutschige Trittsteine balanciert wird. Das ist ein natürlicher Flaschenhals für den Handel.
        
- **Materialien: Holz & Feldstein** Mistledale hat keine großen Steinbrüche, aber Wald ohne Ende.
    
    - _Häuser:_ Solides Fachwerk aus Eiche oder Kiefer, Fundamente aus groben Feldsteinen.
        
    - _Dächer:_ Schiefer (für Reiche/Händler) oder Reet/Stroh (für Bauern). Im Herbst sind die Dächer oft moosbedeckt und feucht.
        
- **Die Nebel-Glocken** Da das Tal oft in dichtem Nebel liegt, hat fast jedes Gehöft und wichtige Gebäude eine eigene Glocke.
    
    - _Flavor:_ Wenn Nebel aufzieht, orientieren sich die Leute nach Gehör. Beschreibe das ferne Läuten, nicht nur das Sehen.

#### 2. Handel & Transport: Der "Moonsea Ride"

Der Fluss ist wichtig, aber die Straße ist die Lebensader.

- **Straße vor Fluss:** Der Ashaba-Fluss ist nördlich der Stadt (Richtung Shadowdale) wegen der Furt und Untiefen kaum schiffbar für große Boote.
    
    - _Konsequenz:_ Der Großteil des Handels läuft über den **Moonsea Ride** (die große Handelsstraße) per Wagen und Ochsenkarren.
        
    - _Szenerie:_ Stau an der Furt; Händler, die Waren von flachen Kähnen auf Wagen umladen.
        
- **Saisonale Güter (Herbst):** Gerade jetzt im Marpenoth (Oktober) werden keine Erdbeeren gehandelt.
    
    - _Was man sieht:_ Wagenladungen voll mit **Rüben, Kartoffeln, Pökelfleisch, Fellen** und Fässern mit **Ale**. Das "Goldene Garbe" (Golden Sheaf) Ale ist ein Exportschlager.

#### 3. Der Cormanthor Wald: Nicht einfach nur "Bäume"

Der Wald ist riesig, aber er hat Zonen. Je tiefer sie gehen, desto anders muss er aussehen.

- **Randgebiet (Rimwood):** Wo die Holzfäller arbeiten.
    
    - _Vegetation:_ Vorwiegend **Kiefern und Nadelbäume** (Blueridge/Needleleaf Pine). Der Boden ist sandig und bedeckt mit braunen Nadeln.
        
    - _Sicht:_ Relativ weit, die Bäume sind "nur" 15-20 Meter hoch.
        
- **Tiefer Wald (Midwood/Starwood):** Wo die Drow und Ruinen lauern.
    
    - _Vegetation:_ Hier stehen die gigantischen **Eichen und Ahornbäume** (Starwood), die bis zu 100 Meter hoch werden können.
        
    - _Licht:_ Selbst tagsüber herrscht hier Zwielicht. Im Herbst bildet das Laub einen modrigen, rutschigen Teppich, der Geräusche schluckt – oder verräterisch raschelt.

### 4. Lokaler "Flavor" für deine Beschreibungen

Hier sind drei kleine Details, die du immer wieder einstreuen kannst:

- **"Das Tal der offenen Türen":** Mistledale gilt als das freundlichste Tal. Leute schließen ihre Türen oft nicht ab (außer nachts wegen der neuen Gefahren).
    
- **Der Geruch:** In Ashabenford riecht es derzeit nach **Holzrauch** (Kamine), **nassem Hund/Fell** (Abenteurer/Jäger) und **gärendem Getreide** (Brauereien).
    
- **Die Reiter:** Man sieht oft die **Reiter von Mistledale** in ihren typischen Plattenpanzern mit dem weißen Pferdesymbol. Sie patrouillieren _auf_ den Wegen, gehen aber ungern _in_ den tiefen Wald.

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
