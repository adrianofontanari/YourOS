---
tags: youros/core, medical
Dimension: Health
---

# ⚕️ Symptoms Log

> [!tip] As your Health Data Hub, this in-line data view query lists the notes with the word "symptom" from the daily journal (in the dedicated "Additional health info..." section). Beware of adding unencrypted Electronic Medical Records or Medical Info as the Obsidian Vault is an open-access folder. Those who can access your laptop can/see/copy the data. The same rule applies to Obsidian in general as the notes are stored in plain text (markdown format).

```dataview TABLE 
TABLE WITHOUT ID (link(file.path)) as Day, symptom as Symptoms FROM #journal/daily
WHERE symptom
SORT file.ctime DESC
```