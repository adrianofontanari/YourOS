---
tags: area/active, area/friends, people/friends, youros/core
Dimension: Relationships
---
# 👭 Friends

> [!tip] As a personal CRM, this dataview query lists the people in the "People" folder with the tag "people/friends". To add a new person, select from the command palette Quickadd: 👤 New Person. Adding a person allows you to tag the person in your journal and have a consolidated page with the linked notes. After creating the Person's page, remember to add the Person's Name in the Alias Properties such as [Person Name] and also in the search target line of the tracker embed: searchTarget: 'Person Name

```dataview
TABLE WITHOUT ID (link(file.path)) as People
FROM "People" AND #people/friends
SORT Asc
```