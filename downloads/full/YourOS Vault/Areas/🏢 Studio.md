---
banner_y: 0.55421
banner: "![[studio.png]]"
cssClasses: cards cards-cols-4
obsidianUIMode: preview
banner_icon: 🏢
Dimension: Mindset
tags: youros/core, area/active
---
# 🏢 Studio

> [!tip] This page serves as a digital studio: find focus by listening to lo-fi music and manage your reading list in a structured way. Are you preparing for an exam? Add the tag 'studio' to your current projects to see them appear here. Are you reading a manual? Add the tag 'studio/reading' to see active books. Are you processing your notes? Add 'studio/output' when you are creating something new for what you learned and 'studio/archive' once no action is required.

```custom-frames  
frame: Studio
style: height: 500px;
```

## 🌳 Projects
```dataview
TABLE WITHOUT ID (link(file.path)) as Projects, Deadline, Priority, Trophy
FROM #project/active AND #studio
SORT Deadline Asc
SORT Priority Asc
```
### 📕 Books
```dataview

TABLE WITHOUT ID (link(file.path)) as Book, ("![coverimg|50](" + Cover + ")") as Cover
FROM #books AND #studio/reading
SORT file.mtime Desc
LIMIT 3
```

## ⏭️ Output
>Output can be: Missing, Tweet, Article, Post, Networking, Internal_Only

```dataview
TABLE WITHOUT ID (link(file.path)) as Title, Output
FROM #studio/output
SORT file.mtime Desc
```

## 🗃️ Archive

```dataview
TABLE WITHOUT ID (link(file.path)) as Title, Output
FROM #studio/archive
SORT file.mtime Desc
LIMIT 5
```