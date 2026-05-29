---
banner_y: 0.6506
banner: "![[journal.png]]"
banner_icon: 📔
tags: youros/core, aboutme
---

#  📔 Journal

> [!tip] This page shows the collection of Journals for each year. Add the tag "journal-showcase" to the year's collection page to see the notes in this data view query

```dataview

TABLE WITHOUT ID (link(file.path)) as Title
from #journal-showcase 
SORT file.mtime Desc
```


## Track the size variation of diaries 
``` tracker
searchType: fileMeta
searchTarget: size
folder: Journal
startDate: 2024-01-01
line:
    title: File Size Variation
    yAxisLabel: Size
    yAxisUnit: bytes
```

## Word counts of daily notes
``` tracker
searchType: fileMeta
searchTarget: numWords, numChars
folder: Journal
startDate: 2024-01-01
datasetName: words, chars
line:
    title: Word Counting
    yAxisLocation: left, right
    yAxisLabel: Words, Characters
    lineColor: red, yellow
    showLegend: true
```

