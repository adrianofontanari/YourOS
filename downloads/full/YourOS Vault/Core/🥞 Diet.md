---
tags: youros/core, medical
Dimension: Health
---
# 🥞 Diet

> [!tip] As your Health Data Hub, this data view query lists the notes with the tag "nutrition" and "recipe. Have you seen a nutritionist and got some dietary info? Would you like to save your favorite meal recipe? This is the right place to do so. Beware of adding unencrypted Electronic Medical Records or Medical Info as the Obsidian Vault is an open-access folder. Those who can access your laptop can/see/copy the data. The same rule applies to Obsidian in general as the notes are stored in plain text (markdown format).


```dataview
TABLE WITHOUT ID (link(file.path)) as "Dietary Notes"
FROM #nutrition
SORT Asc
```

```dataview
TABLE WITHOUT ID (link(file.path)) as "Recipe Book"
FROM #recipe
SORT Asc
```
