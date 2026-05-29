---
banner_y: 0.6506
banner: "![[journal.png]]"
cssClasses: cards cards-cols-4
obsidianUIMode: preview
banner_icon: 📘
tags: youros/core, aboutme
---
# 📘 Life Learnings

> [!tip] This data view query lists all the diary entries in the "Life Learning Log" section of the daily journal. You can add a keyword in the daily journal to classify the life learnings (e.g. l-growth: X, l-mindset: Y). An example of a life-learning could be: "l-health: drinking coffee after 5 pm will impact my sleep". Life learnings will also appear in the growth section of the journal reviews (e.g. weekly reviews).

```dataview TABLE 
TABLE WITHOUT ID (link(file.path)) as Day, life-learning as Life-Learnings FROM #journal/daily
WHERE life-learning
SORT file.ctime DESC
```
