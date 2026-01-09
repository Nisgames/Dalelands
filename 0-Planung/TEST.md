
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