---
title: 'newfangled js'
date: 2024-01-16T14:55:00.001-05:00
draft: false
url: /2024/01/newfangled-js.html
---

things I've come across in the wild lately in js land im adding to my bag of tricks

1.  **Arrow Functions vs. Traditional Functions:**
    
    *   _Arrow Functions (New):_```
        const add = (a, b) => a + b; 
        ```
    *   _Traditional Functions (Old):_```
        const add = function(a, b) {
          return a + b;
        }; 
        ```
    *   **Comparison:**  
        Arrow functions are more concise, especially for simple one-liner functions. They also have a lexical `this` and no binding of their own `this`, making them useful for certain scenarios.
2.  **Destructuring Assignment vs. Traditional Assignment:**
    
    *   _Destructuring Assignment (New):_```
        const [first, second] = [1, 2]; 
        ```
    *   _Traditional Assignment (Old):_```
        const first = arr[0];
        const second = arr[1]; 
        ```
    *   **Comparison:**  
        Destructuring is more concise and expressive when extracting values from arrays or objects. It reduces the need for multiple lines of assignment statements.
3.  **Template Literals vs. String Concatenation:**
    
    *   _Template Literals (New):_```
        const greeting = `Hello, ${name}!`; 
        ```
    *   _String Concatenation (Old):_```
        const greeting = "Hello, " + name + "!"; 
        ```
    *   **Comparison:**  
        Template literals provide a cleaner and more readable way to concatenate strings, especially when including variables or expressions within the string.
4.  **Default Parameters vs. Manual Default Values:**
    
    *   _Default Parameters (New):_```
        function greet(name = "Guest") { /* ... */ } 
        ```
    *   _Manual Default Values (Old):_```
        function greet(name) {
          name = name || "Guest";
          // ...
        } 
        ```
    *   **Comparison:**  
        Default parameters offer a more explicit and less error-prone way to define default values for function parameters.
5.  **Spread Syntax vs. Concatenation:**
    
    *   _Spread Syntax (New):_```
        const arr2 = [...arr1, 4, 5]; 
        ```
    *   _Concatenation (Old):_```
        const arr2 = arr1.concat([4, 5]); 
        ```
    *   **Comparison:**  
        Spread syntax is concise and provides a more visually appealing way to merge arrays or objects.
6.  **Object Literal Enhancements vs. Traditional Object Creation:**
    
    *   _Object Literal Enhancements (New):_```
        const point = { x, y, draw() { /* method implementation */ } }; 
        ```
    *   _Traditional Object Creation (Old):_```
        const point = {
          x: x,
          y: y,
          draw: function() { /* method implementation */ }
        }; 
        ```
    *   **Comparison:**  
        Object literal enhancements reduce redundancy and make the syntax more concise for defining properties and methods.
7.  **Promises/Async-Await vs. Callbacks:**
    
    *   _Promises/Async-Await (New):_```
        async function fetchData() {
          const data = await fetchDataFromAPI();
          console.log(data);
        } 
        ```
    *   _Callbacks (Old):_```
        fetchDataFromAPI(function(data) {
          console.log(data);
        }); 
        ```
    *   **Comparison:**  
        Promises and async-await provide a more structured and readable way to handle asynchronous operations compared to nested callbacks.