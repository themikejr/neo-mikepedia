---  
share: true  
---  
up :: [∴ Software Development](./%E2%88%B4-Software-Development.md)  
  
# Reactivity  
**Reactivity** is the idea that when a program mutates a value that is consumed elsewhere, all downstream usages of the value are updated automatically. The common example of this is a spreadsheet. When the value of a cell is changed, all cells including a formula that depend on the changes value update automatically. The current state of the discussion is informed by ideas from **Declarative** and **Functional** programming styles. There are few commonly used terms related to **reactivity**:  
  
**Effects**, from *side effects*, are changes that flow in to a program. Think of *effecting change*. A function that mutates state that is shared by others is said to have caused a side effect.    
  
**Dependencies** are usually values that are said to cause an effect. When a dependency changes (like one value in a spreadsheet formula), certain effects will need to be run again.  
  
**Subscribers** are effects that are causally connected to their dependencies. An **effect** is said to **subscribe** to a **dependency** when it updates as the **dependency** is mutated.  
  
# References  
  
*What Is Reactivity?*, [vuejs.org](https://vuejs.org/guide/extras/reactivity-in-depth.html#what-is-reactivity)  
  
