---  
share: true  
comments: true  
title: "My Spark Workflow"  
---  
up :: [∴ PKM](./%E2%88%B4-PKM.md)  
  
# My Sparks Workflow  
  
Throughout the day my brain is generating questions, ideas, and connections. If I don't record them so that I know I can find them later, I tend to wonder if 50% of what my brain is doing in a given day is a waste! To combat this **FOMO** of my own ideas, I've found a helpful workflow in my PKM system.   
  
In my daily note, I keep a bulleted list that I treat as a log. It contains things that happened, ideas that I had, etc... When I have an idea that seems like it might be a good one, I prefix it with the tag `#spark`. For example:  
  
```markdown  
2023.03.01  
  
- 30 minute run  
- #spark familiarity makes us blind  
- too many meetings today  
```  
  
Then, at some regular interval (or whenever I feel like it), I can review all of the bullet points in my daily log that have been tagged with `#spark`. From there I can decide if these need to become new notes, projects, or something else. I do this with a query via the **dataview** Obsidian plugin:  
  
```markdown  
LIST without id  
L.text  
FROM "Pensees"  
FLATTEN file.lists as L  
WHERE contains(L.tags, "#spark")  
```  
  
This way, I can quickly capture what might be interesting ideas with no fear of losing sight of them later.