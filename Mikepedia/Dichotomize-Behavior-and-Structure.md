---  
share: true  
title: "Dichotomize Structure and Behavior"  
comments: true  
---  
up [∴ Software Development](./%E2%88%B4-Software-Development.md)  
  
# Dichotomize Behavior and Structure  
*What I do and how I work are two sides of the same coin, but don't change both at the same time.*  
  
When modifying a program, think of changes to **structure** or **behavior** as atomic transactions -- only one should be modified at a time. Changing both at one is too much!  
  
The **structure** of code is not the same thing as its **behavior**. The same **behavior** can be expressed through multiple **structures**. **Behavior** is observed by comparing inputs with outputs. **Structure** is expressed through organization by means of abstraction, coupling, cohesion, and the like. **Structure** can be assessed through the lens of goals, principles, and patterns of **design**. **Behavior** can be assessed with various functional testing techniques.  
  
Both **structure** and **behavior** contribute to the value a system provides and it's attributes. **Structure** has strong affinity with what it is like to *work on* a system --- how easy it is to change, how understandable it is, and what exists in the **adjacent possible** for new functionality. **Behavior** has strong affinity with what it is like to *work with* (i.e. *use* or *consume*) a system -- how easy it is to interact with, integrate with, and derive utility from.  
  
Do not be confused --- **form** and **function** should not be bifurcated in design considerations. **Form** influences **function** and vice versa. **Form** and **Function** or **Structure** and **Behavior** both contribute to the overall experience of interacting with *the thing*. One has to evaluate both when considering *the thing* as they both impact what the thing is. This is not the same as modifying both simultaneously.  
  
# References  
  
[Kent Beck](https://twitter.com/KentBeck/status/1636378506866335745):  
  
> One hat at a time: change the behavior of the system or change the structure. Changing both introduces too much wiggle.  
  
  
[Joe Natoli](https://www.youtube.com/watch?v=BfHRqVp6oTw), *The big lie: why form doesn't and shouldn't follow function*:  
  
> every force evolves form.