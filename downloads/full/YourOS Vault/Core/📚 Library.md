---
banner_y: 0.6506
banner: "![[library.png]]"
cssClasses: cards cards-cols-4
obsidianUIMode: preview
banner_icon: 📚
tags: youros/core, books
---
# 📚 Library

>[!failure] [[📕 Antilibrary]]

>[!info] This page shows a dataview table that lists the notes in the "Books" folder

## All Books
```dataview

TABLE WITHOUT ID (link(file.path)) as Title, ("![coverimg|50](" + Cover + ")") as Cover, Author
from "Books"
SORT file.mtime Desc
```
