---
tags: youros/core, tag
tags: task
title: Tasks
Total: 7
Completed: 2
Incomplete: 5
banner_icon: 🌿
---
# 🌿 This Week

> [!activities]
> • [[🪴 Today]] • [[☘️ Upcoming]]  • [[🌿 This Week]] • [[👨🏼‍🌾 Garden]] 
> • [[🌻 Areas]] • [[🌳 Projects|🌳 Projects]] • [[Journal/TasksLog/Tasks Log - 2024|✅ Tasks Log]] • [[🔁 Periodic]]

> [!tip] This page shows the activities planned for this week. Edit this page to update the list of tasks appearing in Today and Upcoming. New tasks added via quick capture (CMD + T) will be added here with today as the due date. It is good practice to update the list once a week (during the review) and move the completed activities to the [[Journal/TasksLog/2024|✅ Tasks Log]]. To collect the tasks select from the command palette: "Task Collector (TC): Mark task".

---
## 🗓️ Weekly Priorities
![[🪴 Today#^weekly-priorities]]

###### Weekly points:
```dataviewjs
function projectTracker(dv, query) {
    let searchPagePaths = dv.pages(query).file.path
    
    for(let i=0; i < searchPagePaths.length; i++){
        if(dv.page(searchPagePaths[i]).Total){
                    let title = dv.page(searchPagePaths[i]).title;
                    console
                    let total = dv.page(searchPagePaths[i]).Total;
                    let status = ((dv.page(searchPagePaths[i]).Completed / dv.page(searchPagePaths[i]).Total) * 100).toFixed();
                    const progress = "![pb|500](https://progress-bar.dev/" + status + "/?scale=" + "100" + "&title=" + title + "&width=300)"; //you could set any width if you need
                    dv.paragraph(progress);
                    dv.paragraph("<br>"); //use this if you have many projects to track.
        }
    }
} 

projectTracker(
    dv,
    "#task" //change tag if you need
)
```
---
## To do (added during the week - not planned):
 This is a task

---
## Planned

### Monday
- [ ] This is a task - 📅 2024-01-15


### Tuesday
- [x] This is a task ✅ 2024-01-22

### Wednesday
- [x] This is a task ✅ 2024-01-22

### Thursday
- [ ] This is a task

### Friday
- [ ] This is a task

### Saturday
- [ ] This is a task

### Sunday
- [ ] This is a task

## Completed