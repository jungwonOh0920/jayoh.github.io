---
layout: post
author: Jay
---
# ⚡️Arrow functions vs Regular functions

Regular functions with `function` keyword.

```javascript
function hello(person) {
    return `hello, ${person}`
}

const hi = function(person) {
    return `hi, ${person}`
}
```

The arrow function syntax: 
```javascript
const greet = (person) => {
    return `hello, ${person}`
}
```
1. `This` aka "the execution context"
- `This` in regular functions:
    - It's dynamic meaning it depends on how the function is invoked. 
    
    ex 1)
    ```javascript
    function temp() {
        console.log(this)
    }
    
    temp() // prints global object (Window)
    ```
    ex 2) `this` in an object
    ```javascript
    const myObj = {
        print() {
            console.log(this)
        }
    }
    myObj.print() // prints myObj
    ```

- `This` in arrow functions:

Gone camping! ⛺ Be back soon.


<!-- https://dmitripavlutin.com/differences-between-arrow-and-regular-functions/ -->