---
banner_y: 0.6506
banner: "![[journal.png]]"
cssClasses: cards cards-cols-4
obsidianUIMode: preview
banner_icon: 🙏
tags: youros/core, aboutme
---
# 🙏 Gratitude Log

> [!tip] This data view query lists all the diary entries in the "Today I am grateful for..." section of the daily journal

```dataview TABLE 
TABLE WITHOUT ID (link(file.path)) as Day, grateful as Grateful FROM #journal/daily
WHERE grateful
SORT file.ctime DESC
```