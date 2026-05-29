---
<%*
var fileDate = moment(tp.file.title);
// moment dates are mutable
let prevDay = moment(fileDate).subtract(1, 'd').format('YYYY-MM-DD');
let nextDay = moment(fileDate).add(1, 'd').format('YYYY-MM-DD');
let yearLink = fileDate.format('YYYY');
let quarterLink = fileDate.format('YYYY-[Q]Q');
let monthLink = fileDate.format('YYYY-MM');
let weekLink = fileDate.format('gggg-[w]WW');
-%>
tags: daily_note <% fileDate.format("YYYYMMDD") %> <% weekLink %> <% monthLink %> <% quarterLink %> <% yearLink %>
weekday: <% fileDate.format("ddd") %>
banner: "![[journal.png]]"
tags: journal/daily/2024, youros/core
obsidianUIMode: editing
---
# Daily Journal
-----
<%*
// ❮❮ ⋮ 2024 › Q4 › 12 › W49 ⋮ ❯❯
// [[path/to/file|display_text]]
let navStr = `[[Journal/2024/${prevDay}|Yesterday]] ⋮ [[Journal/2024/${yearLink}|${yearLink}]] › [[Journal/2024/${quarterLink}|${fileDate.format('[Q]Q')}]] › [[Journal/2024/2024/${monthLink}|${fileDate.format('MM')}]] › [[Journal/2024/2024/${weekLink}|${fileDate.format('[w]WW')}]] ⋮ [[Journal/2024/${nextDay}|Tomorrow]]`;
tR += navStr
%>

---
## Overview
### Quote of the day:

```localquote-once
search YourOS Life Manifesto
```
- Comment: 
---
### Yearly progress
<%* 
function month() {
    let fileDateNum = fileDate.date();
    let numDays = fileDate.daysInMonth();
    // ignore leapyears
    tR += tp.user.makeProgressBar(fileDateNum, numDays, size=numDays, filledChar = "█", unFilledChar = "◽", label="Month");
}
month();
-%>

<%* 
function year() {
    let dayNum = fileDate.dayOfYear();
    // ignore leapyears
    tR += tp.user.makeProgressBar(dayNum, 365, size=33,filledChar = "█", unFilledChar = "◽", label="Year");
}
year();
%>

----
### Location:

```leaflet
id: Journal
height: 300px
width: 800px
lat: 40.773998
long: -73.966003
minZoom: 10
maxZoom: 100
defaultZoom: 15
unit: meters
scale: 1
marker: default, 40.773998, -73.966003, [[🏠 My Home]
darkMode: true
```

## Journaling

### Today's thoughts/insights...
- 

### The most important thing I must focus on to achieve my goals is... 
>Remember to block your agenda to perform this task
- Morning Comment: 
- Evening Reflection: 

🗓️ Weekly Priorities
![[🪴 Today#^weekly-priorities]]
🪴 Today
```tasks
not done
due today
sort by priority
hide backlink
```

### Reflections:

#### How was my day in a few words (e.g. include factors that influenced well-being)?
- [daily-recap:: ]

#### Today I am grateful for...
- [grateful:: ]

#### A moment to remember
- [memory:: ]

#### Praise Received...
- [praise:: ]

#### Life Learning Log
>Keywords to be added in brackets: growth, identity, work, relationships, health, mindset, financials
- [life-learning:: ]

#### Well-being...
```custom-frames
frame: YourOS Well-being Form
style: height:950px;
```

```custom-frames
frame: YourOS Well-being - daily insights
style: height:240px;
```
```custom-frames
frame: YourOS Trends - Home
style: height:220px;
```
##### how am I performing towards the well-being dimensions? anything I can do today or tomorrow to be more balanced?
- 

#### Additional health info...
- [symptom:: ]
- [medication:: ]

#### 🔖 Log Transaction
```custom-frames
frame: YourOS Financial Transactions Form
style: height:700px;
```

---
## ☘️ Upcoming

### 🪴  Today
```tasks
not done
due today 
sort by priority
hide backlink
```
### 🌼 Tomorrow
```tasks
not done
due tomorrow
sort by priority
hide backlink
```

----
## Activities 

### On this day:

```query 
path:"Journal" file:"{{date:-MM-DD}}" -file:"{{date:YY**}}-"
```
---
### Notes:
```dataview
List
WHERE file.cday = date("<%tp.file.title%>") 
SORT file.ctime asc
```
### Tasks completed:

```tasks 
done on {{date:YYYY-MM-DD}}
```