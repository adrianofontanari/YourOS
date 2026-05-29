---
banner: "![[journal.png]]"
tags: journal/quarterly/2024, youros/core
obsidianUIMode: editing
---
# Quarterly Journal
-----
> [!todo]
> Guide: replace1 = quarter

## Review and Reflect
	Looking Back on the past Quarter:

### 🌳 Projects

#### 🛑 Closed:
```dataview
TABLE WITHOUT ID (link(file.path)) as Projects, Deadline, Priority, Trophy
FROM #project/closed
WHERE Year = 2024 AND Quarter = "replace1"
SORT Deadline Asc
```
#### ✅ Completed:
```dataview
TABLE WITHOUT ID (link(file.path)) as Projects, Deadline, Priority, Trophy
FROM #project/completed 
WHERE Year = 2024 AND Quarter = "replace1"
SORT Deadline Asc
```

### How do I feel about the projects I worked on the past quarter?
	e.g. proud of, went well, biggest challenges, unexpected things, unplanned successes
- 

### How am I different as a person?
- 

^quarterly-growth

## Planning
	Looking Forward to the next quarter:

```dataview
TABLE WITHOUT ID (link(file.path)) as Projects, Deadline, Priority, Category, Trophy
FROM #project/active
WHERE deadline - date(today) <= dur(12 month)
SORT Deadline Asc
SORT Priority Asc
```

#### Are my projects still relevant? If not, set some new ones (it’s okay to let things go that no longer serve me)
- 

###### 🔭 Future outlook
- 

^quarterly-plan

#### What am I most excited about right now?
- 

^quarterly-excitement

#### Where would I like to be in 7 years and with whom?
- 

^quarterly-7y
