---
tags: youros/core
---
# 🗃️ Archive

> [!tip] Following the P.A.R.A. method, this page lists [[🌻 Areas]] that have been archived. For example, did you change your job? Move the old employer's page to this section by changing the tag "area/active" to "area/archived" in the Area's properties.

```dataview
TABLE WITHOUT ID (link(file.path)) as Area, Category
FROM "Core/Areas" and #area/archived
SORT area Asc
```