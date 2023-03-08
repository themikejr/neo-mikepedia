---  
share: true  
---  
up :: [∴ Vue](./%E2%88%B4-Vue.md)  
# Reactivity in Vue  
In Vue, reactivity can be wrapped around values in two different ways: `ref()` and `reactive()`.  
  
**REF** is a wrapper for a single value, like number, string, boolean, and array. Calling `ref(0)` returns an an object that wraps the value with getters and setters that track mutations of the value. Read and mutate refs using `ref.value`. If you provide an object with multiple properties to `ref()`, `reactive()` is used under the hood.,  
  
**REACTIVE** is a wrapper for objects. It uses JavaScript **PROXY** to wrap the object and track mutations. Calling `reactive({ count: 0})` return an object that wraps an equivalent of the original. The newly returned object will not be equal to the original. Access and mutate object properties directly, like `obj.count++`.  
  
See [Reactivity](../Reactivity.md).  
  
# References  
  
*Reactivity in Depth*, [vuejs.org](https://vuejs.org/guide/extras/reactivity-in-depth.html)  
  
*Vue API: `ref`*, [vuejs.org](https://vuejs.org/api/reactivity-core.html#ref)  
  
*Vue API: `reactive`*, [vuejs.org](https://vuejs.org/api/reactivity-core.html#reactive)  
