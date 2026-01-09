
```dataview
TASK
FROM "10_Kampagne/12_Quests"
WHERE !completed
```


```dataview
TASK
FROM "10_Kampagne/12_Quests"
WHERE contains(tags, "#loc/brücke")
AND !completed
```


> [!INFO] Verzweigung 
> **Haben sie dem Dieb geholfen?** 
> - Ja: [[Arc_Diebesgilde#Pfad A - Freunde]] 
> - Nein: [[Arc_Diebesgilde#Pfad B - Feinde]]

