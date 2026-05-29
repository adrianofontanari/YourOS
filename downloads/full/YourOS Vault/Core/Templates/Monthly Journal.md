---
banner: "![[journal.png]]"
tags: journal/monthly/2024, youros/core
obsidianUIMode: editing
---
# Monthly Journal
-----
> [!todo]
> Guide: replace1-4 = weeks of the year, replace5-6: first and last date of the month(full), replace7 first day of the month, replace8 month, replace9 YYYY, replace10 last day of the month, replace11 N of quarter

## Review and Reflect
### Weekly insights

- [[replace1|Week 1]]
	![[replace1#^weekly-recap]]
- [[replace2|Week 2]]
	![[replace2#^weekly-recap]]
- [[replace3|Week 3]]
	![[replace3#^weekly-recap]]
- [[replace4|Week 4]]
	![[replace4#^weekly-recap]]
```custom-frames
frame: YourOS Wellbeing
style: height:950px;
```

```custom-frames
frame: YourOS Well-being Longitudinal Insights
style: height:5100px;
```


##### how was my month in a few words (e.g. include factors that influenced well-being)?
- 

^monthly-recap

#####  What went well?
- 

^monthly-wentwell

- [[replace1|Week 1]]
	![[replace1#^weekly-wentwell]]
- [[replace2|Week 2]]
	![[replace2#^weekly-wentwell]]
- [[replace3|Week 3]]
	![[replace3#^weekly-wentwell]]
- [[replace4|Week 4]]
	![[replace4#^weekly-wentwell]]

##### What didn't go well / What am I personally struggling with right now and should I improve on?
- 

^monthly-struggle

- [[replace1|Week 1]]
	![[replace1#^weekly-struggle]]
- [[replace2|Week 2]]
	![[replace2#^weekly-struggle]]
- [[replace3|Week 3]]
	![[replace3#^weekly-struggle]]
- [[replace4|Week 4]]
	![[replace4#^weekly-struggle]]

##### What should I stop doing?
- 

^monthly-stop

- [[replace1|Week 1]]
	![[replace1#^weekly-stop]]
- [[replace2|Week 2]]
	![[replace2#^weekly-stop]]
- [[replace3|Week 3]]
	![[replace3#^weekly-stop]]
- [[replace4|Week 4]]
	![[replace4#^weekly-stop]]

##### What am I not doing / what should I start doing?
- 

^monthly-do

- [[replace1|Week 1]]
	![[replace1#^weekly-do]]
- [[replace2|Week 2]]
	![[replace2#^weekly-do]]
- [[replace3|Week 3]]
	![[replace3#^weekly-do]]
- [[replace4|Week 4]]
	![[replace4#^weekly-do]]
### Well-being Dimensions
#### General
##### How am I performing towards the well-being dimensions and my routines? Anything I can do to be more balanced?
- 

#### Financials
- 

^monthly-financials

- [[replace1|Week 1]]
	![[replace1#^weekly-financials]]
- [[replace2|Week 2]]
	![[replace2#^weekly-financials]]
- [[replace3|Week 3]]
	![[replace3#^weekly-financials]]
- [[replace4|Week 4]]
	![[replace4#^weekly-financials]]

```custom-frames
frame: YourOS - Financials
style: height:5950px;
```

#### Growth
- 

^monthly-growth

- [[replace1|Week 1]]
	![[replace1#^weekly-growth]]
- [[replace2|Week 2]]
	![[replace2#^weekly-growth]]
- [[replace3|Week 3]]
	![[replace3#^weekly-growth]]
- [[replace4|Week 4]]
	![[replace4#^weekly-growth]]

##### Life: Learnings Log:
```dataview TABLE 
TABLE WITHOUT ID (link(file.path)) as Day, life-learning as Life-Learnings FROM #journal/daily
WHERE life-learning AND file.ctime >= date(replace5) AND file.ctime <= date(replace6)
SORT file.ctime DESC
```
#### Health
- 

^monthly-health

- [[replace1|Week 1]]
	![[replace1#^weekly-health]]
- [[replace2|Week 2]]
	![[replace2#^weekly-health]]
- [[replace3|Week 3]]
	![[replace3#^weekly-health]]
- [[replace4|Week 4]]
	![[replace4#^weekly-health]]

```custom-frames
frame: garmin
style: height: 400px;
```

##### additional health info...
```dataview TABLE 
TABLE WITHOUT ID (link(file.path)) as Day, medication as Medications FROM #journal/daily
WHERE medication AND file.ctime >= date(replace5) AND file.ctime <= date(replace6)
SORT file.ctime DESC
```
```dataview TABLE 
TABLE WITHOUT ID (link(file.path)) as Day, symptom as Symptoms FROM #journal/daily
WHERE symptom AND file.ctime >= date(replace5) AND file.ctime <= date(replace6)
SORT file.ctime DESC
```

#### Relationships
- 

^monthly-relationships

- [[replace1|Week 1]]
	![[replace1#^weekly-relationships]]
- [[replace2|Week 2]]
	![[replace2#^weekly-relationships]]
- [[replace3|Week 3]]
	![[replace3#^weekly-relationships]]
- [[replace4|Week 4]]
	![[replace4#^weekly-relationships]]
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
WHERE praise AND file.ctime >= date(replace5) AND file.ctime <= date(replace6)
SORT file.ctime DESC
```
#### Identity:
- 

^monthly-identity

- [[replace1|Week 1]]
	![[replace1#^weekly-identity]]
- [[replace2|Week 2]]
	![[replace2#^weekly-identity]]
- [[replace3|Week 3]]
	![[replace3#^weekly-identity]]
- [[replace4|Week 4]]
	![[replace4#^weekly-identity]]

##### 🌳 Projects

###### 🛑 Closed:
```dataview
TABLE WITHOUT ID (link(file.path)) as Projects, Deadline, Priority, Trophy
FROM #project/closed
WHERE Year = replace9 AND Quarter = "replace11"
SORT Deadline Asc
```
###### ✅ Completed:
```dataview
TABLE WITHOUT ID (link(file.path)) as Projects, Deadline, Priority, Trophy
FROM #project/completed 
WHERE Year = replace9 AND Quarter = "replace11"
SORT Deadline Asc
```
###### How do I feel about the projects I worked on the past quarter?
	e.g. proud of, went well, biggest challenges, unexpected things, unplanned successes
- 

##### Moments to remember...
- 

^monthly-moment

- [[replace1|Week 1]]
	![[replace1#^weekly-moment]]
- [[replace2|Week 2]]
	![[replace2#^weekly-moment]]
- [[replace3|Week 3]]
	![[replace3#^weekly- moment]]
- [[replace4|Week 4]]
	![[replace4#^weekly-moment]]
##### Examples in which I apply the word of the year (LOVE):
- [[replace1|Week 1]]
	![[replace1#^annual-woy]]
- [[replace2|Week 2]]
	![[replace2#^annual-woy]]
- [[replace3|Week 3]]
	![[replace3#^annual-woy]]
- [[replace4|Week 4]]
	![[replace4#^annual-woy]]

#### Mindset
- 

^monthly-mindset

- [[replace1|Week 1]]
	![[replace1#^weekly-mindset]]
- [[replace2|Week 2]]
	![[replace2#^weekly-mindset]]
- [[replace3|Week 3]]
	![[replace3#^weekly-mindset]]
- [[replace4|Week 4]]
	![[replace4#^weekly-mindset]]
##### What is the elephant in the room? 
- 

^monthly-elephant

##### What created energy? 
- 

^monthly-energy

##### What drained energy? 
- 

^monthly-drained


```dataview TABLE 
TABLE WITHOUT ID (link(file.path)) as Day, grateful as Grateful FROM #journal/daily
WHERE grateful AND file.ctime >= date(replace5) AND file.ctime <= date(replace6)
SORT file.ctime DESC
```
```custom-frames
frame: ActivityWatch
```

## Planning 

### In the upcoming month I will focus on (🗓️ Monthly Priorities):
- I want to (what) so that I can (why) by (how)
	- 

- These things must happen this month...
	- 

- The major deadline of this month includes (REVIEW CALENDAR)...
	- 

- The best ways I can prepare and ensure that I show up to win the upcoming month are...
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


