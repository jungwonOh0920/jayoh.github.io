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
There are mainly 5 things we can see the differences between regular functions and arrow functions.

1. `This` aka "the execution context"
- `This` in regular functions: It's *dynamic* meaning it can change depending on how the function is invoked. 
    
    ex 1)
    ```javascript
    function temp() {
        console.log(this)
    }
    
    temp() // prints global object (Window in browsers)
    ```
    ex 2) 
    ```javascript
    const myObj = {
        print() {
            console.log(this)
        }
    }
    myObj.print() // prints myObj
    ```
    ex 3) 
    ```javascript
    function MyFunction() {
        console.log(this);
    }
    new MyFunction(); // prints an instance of MyFunction
    ```
- `This` in arrow functions: No matther how or where being executed, `this` value inside of an arrow function always equals `this` value from the **outer function**. So, it resolves `this` lexically. Lexical refers the lexical scope (or Static scope) which is that the name resolution depends on the location in the source code and the lexical context, which is defined by where the named variable of function is defined. 

    ```javascript
    const myObject = {
        myMethod(items) {
            console.log(this); // prints myObject
            const callback = () => {
                console.log(this); // prints myObject
            };
            items.forEach(callback);
        }
    };

    myObject.myMethod([1, 2, 3]);
    ```
<!-- Gone camping! ⛺ Be back soon. -->


<!-- https://dmitripavlutin.com/differences-between-arrow-and-regular-functions/ -->