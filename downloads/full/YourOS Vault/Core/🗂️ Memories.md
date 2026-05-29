---
banner_y: 0.6506
banner: "![[journal.png]]"
cssClasses: cards cards-cols-4
obsidianUIMode: preview
banner_icon: 🗂️
tags: youros/core, aboutme
---
# 🗂️ Memories

> [!tip] This data view query lists all the diary entries in the "A moment to remember" section of the daily journal

```dataview TABLE 
TABLE WITHOUT ID (link(file.path)) as Day, memory as Memories FROM #journal/daily
WHERE memory
SORT file.ctime DESC
```