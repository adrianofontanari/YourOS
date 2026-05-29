---
tags: youros/core
---

# ☁️ Projects Memorial

> [!tip] Not all projects/goals are meant to be completed. To close a project in youros change the tag "project/active" to "project/stopped" on the project page. Interrupted projects/goals will be listed on this page.

# Summary

```dataview
TABLE length(rows) as Trophies
FROM #project/stopped
GROUP BY Trophy
SORT Type ASC
```
## Year 2023

```dataview
TABLE WITHOUT ID Trophy AS "Trophies",
(link(file.path)) as Projects, string("Category: ") + category AS "Category"
FROM project/stopped
WHERE year = 2023
SORT Type desc
```