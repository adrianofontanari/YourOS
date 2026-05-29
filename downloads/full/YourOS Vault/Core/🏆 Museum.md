---
tags: youros/core, aboutme
banner_icon: 🏆
banner: "![[museum.png]]"
---

# 🏆 Museum

> [!tip] It is always good to achieve a goal/project. You do not need to be famous to have a personal museum. This space lists completed goals/projects. You can complete a project by changing the tag from "project/active" to "project/completed" in the project's properties. You can add academic achievements (e.g. certifications) in the dedicated section. Additionally, you can add pictures of personal historical moments in the folder "Attachments/Museum". No longer interested in a project/goal? Change the tag from "project/active" to "project/stopped" to add it to the [[☁️ Projects Memorial]].

## 🖼️ Years

###  Summary

```dataview
TABLE length(rows) as Trophies
FROM #goals/completed 
GROUP BY Trophy
SORT Type ASC
```
---

### Year 2024
```dataview
TABLE WITHOUT ID Trophy AS "Trophies", 
(link(file.path)) as Goals, Category, Quarter
FROM #goals/completed 
WHERE year = 2024
SORT Trophy desc
```
---

> [!warning] [[☁️ Projects Memorial]]

##  🏆Trophy Room

### ⚽Sport
(e.g. medals)

### 👨🏼‍🎓 Education 
(e.g. certifications)

### 🔬 Academic Publications
(e.g. papers)

## 📸 Historical Moments

```img-gallery
path: Attachments/Museum
type: vertical
columns: 2
radius: 4
gutter: 8
sort: asc
```
