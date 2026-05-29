---
cssclasses:
  - dashboard
banner_icon: 📆
banner: "![[YourOSHome.png]]"
banner_y: 0.61829
banner_x: 1
tags: youros/core
obsidianUIMode: preview
"":
---
# 🏡 Home

> [!tip]
> The Home page is designed to become the dashboard of your life. Access the full configuration guide here: [[📙 YourOS Handbook]]

````col
```custom-frames  
frame: Time
style: height: 200px;
```

```custom-frames  
frame: Avatar
style: height: 200px;
```

```custom-frames  
frame: Weather
style: height: 200px;
```
````
```search-bar
only search bar
```
```custom-frames
frame: YourOS Wellbeing - insights (home)
style: height:260px;
```
```custom-frames
frame: YourOS Trends - Home
style: height:230px;
```
## ☑️ Task Manager
```tasks
not done
(due today) OR (due before today)
sort by priority
hide backlink
```

[[Core/🌳 Projects|🌳 Projects]]
```dataview
TABLE WITHOUT ID (link(file.path)) as Projects, Deadline, Priority, Category, Trophy
FROM #project/active
WHERE deadline - date(today) <= dur(4 month)
SORT Deadline Asc
SORT Priority Asc
```
----
## ◩ Knowledge Base

- ### Growth
![[Growth.png|170]]
- 
[[🪴 Today]]
[[☘️ Upcoming]] 
[[🌿 This Week]]
[[👨🏼‍🌾 Garden]] 
[[🔁 Periodic]]
[[Core/📚 Library|📚 Library]]
[[👨🏼‍🎓 Education|👨🏼‍🎓 Education]]
[[Core/📜 Quotebook|📜 Quotebook]]

- ### Identity
![[Identity.png|170]]
- 
[[🌳 Projects|🌳 Projects]]
[[👤 About Me|👤 About Me]]
[[🌻 Areas]]
[[🏆 Museum]]
[[🗃️ Archive]]

- ### Relationships
![[Relationships.png|170]]
- 
[[Areas/👩‍👧‍👦 Family|👩‍👧‍👦 Family]]
[[Areas/👭 Friends|👭 Friends]]
[[Areas/🧑‍💼 Work|🧑‍💼 Work]]
[[👭 Acquaintances|👭 Acquaintances]]

- ### Health
![[Health.png|170]]
- 
[[🏥 Medical]]
[[⚡ Well-being Analytics]]
[[⚕️ Symptoms Log]]
[[💊 Medications and Supplements Intake]]
[[Core/🥞 Diet|🥞 Diet]]
[[Core/🏃🏼 Sport|🏃🏼 Sport]]

- ### Mindset
![[Mindset.png|170]]
- 
[[🏢 Studio|🏢 Studio]]
[[Core/🏠 My Home|🏠 My Home]]
[[🛟 YourOS Harbour]]

- ### Financials
![[Financials.png|170]]
- 
[[💰 Financials]]

- ### Tools
![[Tools.png|170]]
- 
[[🛠️ Utilities|🛠️ Utilities]]
[[Core/💾 Backup|💾 Backup]] 
[[🛒 Wish List]]
[[📙 YourOS Handbook|📙 YourOS Handbook]]

---

## ◶ Wellbeing Overview

### Overview
```custom-frames
frame: YourOS Wellbeing
style: height:950px;
```
```custom-frames
frame: YourOS Leaderboard
style: height: 490px;
```
### 👨🏼‍💻 Productivity
#### Weekly points:
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


### Financials

```custom-frames
frame: YourOS Financials - Home
style: height:1150px;
```

## 📱 Widgets

### [[🏆 Museum|🌠 Annual Achievements]] 

```dataview
TABLE length(rows) as Number
FROM #goals/completed
WHERE year = 2023
GROUP BY Trophy
SORT Type ASC
```


> [!multi-column]
> 
>> [!blank-container]+ Radar
>>  ```custom-frames  
>> frame: Paris
>> style: height: 300px;
>> ```
> 
>> [!blank-container]+ Radar
>>  ```custom-frames  
>> frame: Radar
>> style: height: 300px;
>> ```

---
**Copyright: [Adriano Fontanari](https://adrianofontanari.com/) ([@adryhealth](https://twitter.com/adryhealth)) - Unauthorized distribution of YourOS is strictly prohibited**