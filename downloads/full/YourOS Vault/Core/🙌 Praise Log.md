---
banner_y: 0.6506
banner: "![[journal.png]]"
cssClasses: cards cards-cols-4
obsidianUIMode: preview
banner_icon: 🙌
tags: youros/core, aboutme
---
# 🙌 Praise Log

> [!tip] This data view query lists all the diary entries in the "Praise Received..." section of the daily journal

```dataview TABLE 
TABLE WITHOUT ID (link(file.path)) as Day, grateful as Grateful FROM #journal/daily
WHERE praise
SORT file.ctime DESC
```