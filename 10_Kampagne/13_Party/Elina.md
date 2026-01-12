---
tags:
  - PC
Volk: Eladrin
Klasse: Waldläuferin
hp: "25"
ac: "14"
level: 3
modifier: 0
Spieler: "[[Alina]]"
---

## Persönlichkeit

- Je nach Jahreszeit ihrer Eladrin-Herkunft

|**Jahreszeit**|**Emotionale Ausprägung**|
|---|---|
|**Frühling**|Fröhlich, energetisch, neugierig, optimistisch.|
|**Sommer**|Leidenschaftlich, mutig, reizbar, aggressiv.|
|**Herbst**|Gütig, hilfsbereit, freundlich, ruhiger.|
|**Winter**|Melancholisch, distanziert, nachdenklich, zynisch.

- **Eigenschaften:** Wachsam und teils abergläubisch. Sie interpretiert vieles als „höheres Zeichen“ und führt ein Notizbuch für ihre Beobachtungen.
- **Bewältigung:** Verdrängt ihre tragische [[Elina#Hintergrundgeschichte|Geschichte]] konsequent.
- **Ziele:** Sucht nach ihrem tieferen Sinn und ihrer Aufgabe im Leben.
- **Tierliebe:** Tötet oder bekämpft keine Tiere, verharmlost sogar gefährliche Kreaturen und ist sehr ungern ohne tierische Begleitung alleine.
- **Gesinnung:** Neutral Gut.

## Aussehen

- normale Statur, sportlich
- offene, wellige Haare
- spitze Ohren (Elf)
###### Frühling
- braune Haare, grüne Augen
###### Sommer
- goldene Haare, grüne Augen
###### Herbst
- orangene Haare, rötliche Augen, dunklere Haut
###### Winter
- weiße Haare, blaue Augen, helle Haut

## Hintergrundgeschichte

- **Herkunft:** Lebte mit ihrer Familie in [[Myth Drannor]].
- **Trauma:** Überlebte als Einzige aus ihrem Umfeld die Zerstörung der Stadt.
- **Aktueller Wohnort:** Floh nach [[Ashabenford]] und lebt dort seit 10 Jahren.
- **Berufung:** Arbeitet als Guide; ihr Leben besteht aktuell nur aus „Side-Quests“.

#### Bekanntschaften

[[Baumhirte Steffen]] 
- **Kennenlernen:** Sie hat ihn während einer Quest kennengelernt, bei der sie den Auftrag hatte, ihm seltene Kräuter zu bringen.
- **Regelmäßiger Kontakt:** Die beiden treffen sich einmal pro Woche und rauchen dann gemeinsam Pfeife.    

[[Halbling-Familie Wiesengrund]]
- **Hintergrund:** Die Familie ist sehr wohlhabend („sehr reich“), da sie auf ihren Ländereien einen Schatz ausgegraben haben.
- **Aktueller Status:** Sie befinden sich momentan auf einer Weltreise.
- **Beziehung:** Die Spielerin hat die Familie als „Touri-Guide“ herumgeführt.

## Sessions
#### Teilgenommen
```dataview
TABLE WITHOUT ID
	file.link as Session,
	DM as DM,
	date as Datum
FROM #Session AND !"3-DM"
WHERE
	contains(Players, this.file.link)
SORT date ASC
```
#### Nicht teilgenommen
```dataview
TABLE WITHOUT ID
	file.link as Session,
	DM as DM,
	date as Datum
FROM #Session AND !"3-DM"
WHERE
	!contains(Players, this.file.link)
SORT date ASC
```
