---
tags: youros/core, aboutme
banner_icon: 🌳
---
# 🌳 Projects

> [!activities]
> • [[🪴 Today]] • [[☘️ Upcoming]]  • [[🌿 This Week]] • [[👨🏼‍🌾 Garden]] 
> • [[🌻 Areas]] • [[🌳 Projects|🌳 Projects]] • [[Journal/TasksLog/Tasks Log - 2024|✅ Tasks Log]] • [[🔁 Periodic]]

> [!tip] This page shows the active projects in the short-term (next 12 months), mid-term (next 2-4 years), and long-term (>5 years). Completed projects will appear in the [[🏆 Museum]]. Note: YourOS treats goals as projects (to make things happen goals should be projects with a defined deadline). You can add new projects by selecting New Project from the command palette menu. To see PDF files in the folder of a specific project, add the folder name to the data view query on the project page.

----
### Short-term (next 12 months)

```dataview
TABLE WITHOUT ID (link(file.path)) as Projects, Deadline, Priority, Category, Trophy
FROM #project/active
WHERE deadline - date(today) <= dur(13 month)
SORT Deadline Asc
SORT Priority Asc
```

### Mid-term (2-4 years)

```dataview
TABLE WITHOUT ID (link(file.path)) as Projects, Deadline, Priority, Category, Trophy
FROM #project/active
WHERE deadline - date(today) > dur(13 month)
WHERE deadline - date(today) <= dur(48 month)
SORT Deadline Asc
SORT Priority Asc
```
### Long-term (>5 years)

```dataview
TABLE WITHOUT ID (link(file.path)) as Projects, Deadline, Priority, Category, Trophy
FROM #project/active
WHERE deadline - date(today) > dur(48 month)
SORT Deadline Asc
SORT Priority Asc
```
---

> [!success] [[🏆 Museum|Access 🏆 YourOS Museum]]

----
#### 🌠 Project/Goal Rewards Guide

- Daily
	- **DEFINITION:** A successful project that requires a few days of work
		**EXAMPLE:** Write an article for the website
		**REWARD:** 🛴
- Weekly
	- **(1) DEFINITION:**  A successful  project that requires a few weeks of work
		- **EXAMPLE:** Write a report for the website
		- **REWARD:** 🛵
- Performance-based
	- **DEFINITION:**  Reach a goal based on a continuous commitment (it depends mostly on you) - can include tier 2,3 only, the focus is on consistency
	- **EXAMPLE:** Adherence to routines (e.g. read a book 80% of times)
	- **REWARD:** 🚗 
- Monthly
	- **DEFINITION:** A successful project that requires a few months of work or adherence to routines Tier 1 goals
	- **EXAMPLE:** Learn Python Fundamentals
	- **REWARD:** 🏎  
- (mostly) Performance-based
	- **DEFINITION:** Reach a goal (expected) based on performance (it depends also on external factors) - can include tier 1,2 only
	- **EXAMPLE:** Get a salary raise
	- **REWARD:** 🚁  
- Performance-based
	- **DEFINITION:**  🛩️  Reach a goal (more than what was expected) based on performance (it depends also on external factors) - can include tier 1 only
	- **EXAMPLE:** Change Job, Job promotion
	- **REWARD:** 🛩️  
- Inspirational
	- **DEFINITION:** Life-changing goals
	- **EXAMPLE:** Buy a House
	- **REWARD:** ✨
