---
tags:
  - NPC
Status: Lebendig
Volk: Mensch
Klasse: Händler
Level:
Ort: "[[Ashabenford]]"
Fraktionen: "[[Zhentarim]]"
Rolle: Händler
Relevanz: Hoch
statblock: inline
---

## Erscheinung

*Klasse/Beruf:* `=this.Klasse` 
*Volk:* `=this.Volk` 
*Wohnort:* `=this.Ort` 
*Aussehen:* 
	[Klein mit Bart]
*Charakterzug:* 
	[Hasst Wein]
*Sprechweise:* 
	[Langsam]

## Werte & Loot:

> [!statblock]-
> ![]

> [!loot]- Loot 
> - Der Gehstock (ist eigentlich eine getarnte Degenscheide oder enthält ein Fach für Giftphiolen). 
> - Ein Siegelring mit dem Wappen von [[Sembia]] (Fake). 
> - Schlüsselbund für das [[Thornes Kontor]]. 
> - Notizbuch mit verschlüsselten Transaktionen ("Lieferung S. an Z.").

## DM Wissen

* **Wahre Loyalität:** Er ist ein **Aranea** (Spinnen-Rang) der [[Zhentarim]]. Er berichtet direkt an die Führer in Darkhold oder Mulmaster.
* **Beziehung zu Kaelen:** Er verachtet [[Kaelen]] und dessen brutale Methoden. Er sieht Kaelen als "notwendiges Übel" für die Drecksarbeit, würde ihn aber jederzeit opfern.
* **Plan:** Er will das Monopol auf den Handel mit [[Schattensplitter]]n. Er nutzt die Abenteurer, um die Splitter zu finden (von Drow, [[Drachenkult]] oder Ruinen), bezahlt sie gut ("ehrliche Arbeit") und verkauft die Ware dann für das Zehnfache weiter.
* **Der Verrat:** Sobald die Spieler zu viel wissen oder sich weigern, Splitter abzugeben, arrangiert er einen "Unfall" oder lädt sie zu einem vergifteten Abendessen ein.

#### Begegnungen
```dataview
list without id link(file.link, title)
from #Session and !"00_Admin/03_Templates"
where contains(file.outlinks, this.file.link)
sort file.name asc
```
#### Plots
```dataview
table without id file.link as "Plot", category as "Kategorie"
from #Plot and !"00_Admin/03_Templates"
where contains(file.outlinks, this.file.link)
sort category asc
```
#### Items in Besitz
```dataview
list without id link(file.link, title)
from #Item and !"00_Admin/03_Templates"
where besitzer = this.file.link
sort file.name asc
```