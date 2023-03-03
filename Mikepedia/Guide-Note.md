---  
share: true  
comments: true  
title: "Guide Note"  
---  
up :: [PKM for Coders](./PKM-for-Coders.md)  
  
# Guide Note  
  
When learning a new tool or technology it takes time for the commands and **API** to seep into our muscle memory. Of course, for tools that we are using in the long term, the goal is to be able to work with them directly without the need for reference material. Until one reaches that point though, it's helpful to distill commands, processes, and other actions into a note for quick reference. This is the purpose of a **Guide Note**.  
  
The **Guide Note** should be *easily accessible*. You can accomplish this by linking to it in a higher-order note related to your current learning.  
  
The **Guide Note** should *contain examples*. Add the commands, API methods, keyboard shortcuts, or code snippets that are just enough to job your memory.  
  
The **Guide Note** should be *short lived*. The goal is not to make yourself dependent on the note but rather to make the process of learning more efficient.  
  
## An Example  
Imagine that your are just beginning to learn **Git** for version control. Running **Git** commands will become an important part of your workflow but is interspersed with all of your other tasks such that each time you need to run some **Git** commands, you have trouble remembering what you learned the previous day. In this case, create a **Git Guide** for yourself:  
  
````markdown  
up :: [Learning to Code]  
  
# Git Guide  
  
## Add all changed files to staging  
  
````shell  
git add .  
```  
  
## Commit with a short message  
  
```shell  
git commit -m "<message here>"  
```  
  
## Push changes to github  
  
```shell  
git push  
```  
````  
  
  
Obviously, we don't want to be consulting this note every time we work with **Git** for the rest of our lives, but we also don't want to have to google the commands each time we need them. While we're still learning, the **Guide Note** is a way to improve our efficiency.