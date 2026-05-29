---
banner: "![[journal.png]]"
tags: journal/weekly, youros/core
obsidianUIMode: editing
---
# Weekly Journal
-----

## Review and Reflect
### Daily insights
 ```dataview TABLE 
TABLE WITHOUT ID (link(file.path)) as Day, daily-recap as Daily-Recap
FROM #journal/daily
WHERE daily-recap AND file.ctime >= date(2024-02-05) AND file.ctime <= date(2024-02-12)
SORT file.ctime Asc
```
```custom-frames
frame: YourOS Wellbeing
style: height:950px;
```
```custom-frames
frame: YourOS Well-being Longitudinal Insights
style: height:5100px;
```
##### how was my week in a few words (e.g. include factors that influenced well-being)?
- 

^weekly-recap

#####  What went well?
- 

^weekly-wentwell

##### What didn't go well / What am I personally struggling with right now and should I improve on?
- 

^weekly-struggle

##### What should I stop doing?
- 

^weekly-stop

##### What am I not doing / what should I start doing?
- 

^weekly-do

### Well-being Dimensions

#### General
##### How am I performing towards the well-being dimensions and my routines? Anything I can do to be more balanced?
- 

#### Financials
- 

^weekly-financials

```custom-frames
frame: YourOS - Financials
style: height:6250px;
```
#### Growth
- 

^weekly-growth

##### Life: Learnings Log:
```dataview TABLE 
TABLE WITHOUT ID (link(file.path)) as Day, life-learning as Life-Learnings FROM #journal/daily
WHERE life-learning AND file.ctime >= date(2024-02-05) AND file.ctime <= date(2024-02-12)
SORT file.ctime DESC
```
##### Latest Notes:

```dataview
TABLE WITHOUT ID (link(file.path)) as Note, file.ctime AS "Creation Date"
WHERE file.ctime >= date(2024-02-05) AND file.ctime <= date(2024-02-12)
SORT file.ctime Asc
```
#### Health
- 

^weekly-health

##### additional health info...
```dataview TABLE 
TABLE WITHOUT ID (link(file.path)) as Day, medication as Medications FROM #journal/daily
WHERE medication AND file.ctime >= date(2024-02-05) AND file.ctime <= date(2024-02-12)
SORT file.ctime DESC
```
```dataview TABLE 
TABLE WITHOUT ID (link(file.path)) as Day, symptom as Symptoms FROM #journal/daily
WHERE symptom AND file.ctime >= date(2024-02-05) AND file.ctime <= date(2024-02-12)
SORT file.ctime DESC
```

#### Relationships
- 

^weekly-relationships

##### 👩‍👧‍👦 Family
```dataview
TABLE WITHOUT ID (link(file.path)) as People
FROM "People" AND #people/family
SORT Asc
```
##### 👭 Friends
```dataview
TABLE WITHOUT ID (link(file.path)) as People
FROM "People" AND #people/friends
SORT Asc
```
```dataview TABLE 
TABLE WITHOUT ID (link(file.path)) as Day, praise as Praise FROM #journal/daily
WHERE praise AND file.ctime >= date(2024-02-05) AND file.ctime <= date(2024-02-12)
SORT file.ctime DESC
```
#### Identity:
- 

^weekly-identity

##### moments to remember...
- 

^weekly-moment

```dataview TABLE 
TABLE WITHOUT ID (link(file.path)) as Day, memory as Memories FROM #journal/daily
WHERE memory AND file.ctime >= date(2024-02-05) AND file.ctime <= date(2024-02-12)
SORT file.ctime DESC
```

```dataview TABLE 
TABLE WITHOUT ID (link(file.path)) as Day, grateful as Grateful FROM #journal/daily
WHERE grateful AND file.ctime >= date(2024-02-05) AND file.ctime <= date(2024-02-12)
SORT file.ctime DESC
```

###### Examples in which I apply the word of the year (Love):
- 

^annual-woy

#### Mindset
- 

^weekly-mindset

```dataview
TASK 
WHERE completion >= date(2024-02-05) AND completion < date(2024-02-12)
```

## Planning: 

### How did I perform toward my weekly priorities? in which area am I falling short?
![[🪴  Today#^weekly-priorities]]

### In the upcoming week I will focus on (🗓️ Weekly Priorities):
- I want to (what) so that I can (why) by (when)
	- 

- Hence, these are the things that must happen this week (how)...
	- 

- The major deadline of this week includes (REVIEW CALENDAR)...
	- 

- The best ways I can prepare and ensure that I show up to win the upcoming week are...
	- 

### How am I performing toward my projects? Is any review needed?
- 
```dataview
TABLE WITHOUT ID (link(file.path)) as Projects, Deadline, Priority, Category, Trophy
FROM #project/active
WHERE deadline - date(today) <= dur(12 month)
SORT Deadline Asc
SORT Priority Asc
```
