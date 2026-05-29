---
tags: youros/core
---
# 👨🏼‍🎓 Education

>[!tip] This page shows a dataview table that lists the notes with the  "education" tag. Education pages could refer to the title of a university major (e.g. MSc in Artificial intelligence); the sub-pages could include the courses.

```dataview

TABLE WITHOUT ID (link(file.path)) as Title, ("![coverimg|50](" + Cover + ")") as Cover, Topic
FROM "Areas/Sub-Areas" AND #education
SORT file.mtime Desc
```
