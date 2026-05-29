---
tags: youros/core
banner_icon: 🪴
---
# 🪴 Today

> [!activities]
> • [[🪴 Today]] • [[☘️ Upcoming]]  • [[🌿 This Week]] • [[👨🏼‍🌾 Garden]] 
> • [[🌻 Areas]] • [[🌳 Projects|🌳 Projects]] • [[Journal/TasksLog/Tasks Log - 2024|✅ Tasks Log]] • [[🔁 Periodic]]

> [!tip] This page shows the activities due today. It also includes the weekly priorities, an inbox for notes with the tag "inbox", and a scratch book

---

## 🗓️ Weekly Priorities
- [ ] This is a Task


^weekly-priorities

### Progress:

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
## ✏ Scratch book


---
## 📥 Inbox

```dataview
TABLE WITHOUT ID (link(file.path)) as Note
FROM #inbox
```

## ✅ Tasks 

### ⏰ Due Today
> [!multi-column]
> 
>>[!blank-container]+ Hours
>> ### 🚨 Urgent
>>```tasks
>>not done
>>due today
>>sort by tag
>>tag includes #tasks/time-sensitive
>>hide backlink
>>```
>
>>[!blank-container]+ Weather
>>### ‼️ Overdue
>>```tasks
>>not done
>>due before today
>>sort by tag
>>hide backlink
>>```
### 👨🏼‍💻 Focus
```tasks
not done
due today and before today
tag does not include #tasks/time-sensitive
sort by priority
hide backlink
```
