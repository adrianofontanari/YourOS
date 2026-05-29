---
tags: area/active, youros/core
Dimension: Health
---

# 🏥 Medical

> [!tip] As your Health Data Hub, this data view query lists the notes with the tag "medical". Beware of adding unencrypted Electronic Medical Records or Medical Info as the Obsidian Vault is an open-access folder. Those who can access your laptop can/see/copy the data. The same rule applies to Obsidian in general as the notes are stored in plain text (markdown format).

```dataview
TABLE WITHOUT ID (link(file.path)) as "Medical Notes"
FROM #medical
SORT Asc
```