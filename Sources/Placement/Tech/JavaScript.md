# Source: JavaScript Notes

# JavaScript Notes

<aside>
💡

**Notion Tip:** Use this template to write quick notes you can reference later and quickly create a rich document. You can embed links, images, to-do’s, and more. Learn more about the different types of content blocks [here](https://www.notion.so/help/guides/types-of-content-blocks).

</aside>

# JavaScript Language

---

JavaScript is a versatile programming language that is primarily used for web development. Here are the key points about JavaScript:

- It's a high-level, interpreted programming language that enables interactive web pages
- It runs in web browsers and can also be used on servers (Node.js)
- It allows you to add dynamic behavior, handle user interactions, and update content in real-time
- It's one of the core technologies of the web, alongside HTML and CSS

---

## Primitive Types

—> 7 primitive types:

- Null
- Number
- String
- Symbol
- Boolean
- BigInt
- Undefined

```jsx
let a = null;
let b = 243;
let c = true;
let d = BigInt("443");
let e = "hello";
let f = Symbol("hello vai kya haal chaal");
let g = undefined;
console.log(a, b, c, d, e, f, g);
console.log(typeof c);
```

The code will output:

```
null 243 true 443n "hello" Symbol(hello vai kya haal chaal) undefined
boolean
```

This code demonstrates the different primitive types in JavaScript. It declares variables for each primitive type (null, number, boolean, BigInt, string, Symbol, and undefined)and then logs their values and the type of variable 'c' (which is boolean).

## Objects

Objects in JavaScript are one of the non-primitive data types, distinct from the seven primitive types(null, number, string, symbol, boolean, bigint, and undefined).

Here's a suggested explanation you can add at your cursor location:

```jsx
// Objects are collections of key-value pairs
let person = {
    name: "John",
    age: 30,
    isStudent: false
};
```

**Objects are used to store collections of related data and functionality in key-value pairs**. 

Unlike primitive types which store a single value, objects can hold multiple values and methods.

```jsx
const m = {
  "harry": true,
  "shubh": false,
  "lovish": 67,
  "rohan": undefined
}
console.log(m["shubh"])
console.log(m.lovish)
```

The code will output:

```jsx
false
67
```

This output is because m["shubh"] accesses the value of the "shubh" key (which is false), and m.lovish accesses the value of the "lovish" key (which is 67).

## Functions in JavaScript

Let me provide you with code examples for JavaScript functions that you can add at your cursor location:

```jsx
// Basic function declaration
function greet(name) {
    return "Hello " + name;
}

// Function expression
const multiply = function(a, b) {
    return a * b;
};

// Arrow function
const add = (a, b) => a + b;

// Function with default parameters
function welcome(name = "Guest") {
    return "Welcome " + name;
}
```

Key points about JavaScript functions:

- Functions are blocks of reusable code that can be called multiple times
- They can be used to handle user interactions and update content dynamically
- Functions are a fundamental part of JavaScript as one of the core web technologies

There are several ways to write functions in JavaScript, including regular function declarations, function expressions, and arrow functions.

```jsx
let x = 4
let y = 3
let z = 23

function avg(x,y){
  let sum = x+y
  console.log("Done")
  return 1+(sum/2);
}

console.log ("One plus Average of x and y is:", avg(x,y))
```

When this code runs, it will output:

```jsx
Done
One plus Average of x and y is: 4.5
```

This is because:

- The function avg(x,y) first prints "Done"
- Then it calculates (4+3)/2 = 3.5
- Finally it adds 1 to that result: 1 + 3.5 = 4.5

### Arrow Function

```jsx
const hell=()=>{
  console.log("hey how are you")
  return "hi"
}
```

- Arrow functions are just a different representation of function expressions.
- Function expressions use variables to store functions, while function declarations are hoisted to the top of the program.
- Arrow functions don’t create their own this scope. They retain the parent’s context.

## Lexical This

In JavaScript, **`this`** refers to the context in which a function is executed. The value of `this` can change depending on how and where the function is called. However, **lexical `this`** behaves differently—it is determined based on where a function is **defined**, not where it is **called**.

---

### Key Points About Lexical `this`

1. **Arrow Functions**:
    - Arrow functions introduced in ES6 do not have their own `this`.
    - Instead, they **lexically inherit `this`** from the surrounding (enclosing) scope where they are defined.
2. **Difference From Regular Functions**:
    - Regular functions have their own `this`, which is determined dynamically based on how the function is invoked (e.g., via an object, `call()`, or `apply()`).
    - Arrow functions do not change their `this` value based on the invocation context.

---

### Examples

### Regular Function (Dynamic `this`):

```jsx
function Person(name) {
  this.name = name;
}

Person.prototype.sayName = function () {
  console.log(this.name); // `this` refers to the calling object
};

const person1 = new Person("Alice");
person1.sayName(); // Output: Alice

const detached = person1.sayName;
detached(); // Output: undefined (or error in strict mode), because `this` is undefined in this context

```

### Arrow Function (Lexical `this`):

```jsx
function Person(name) {
  this.name = name;

  // Arrow function does not have its own `this`, it uses the `this` from the enclosing scope.
  this.sayName = () => {
    console.log(this.name);
  };
}

const person1 = new Person("Alice");
person1.sayName(); // Output: Alice

const detached = person1.sayName;
detached(); // Output: Alice, because `this` is lexically bound to `person1`

```

---

### **Why Lexical `this` is Useful**

1. **Avoid `this` Confusion**:
    - In callbacks or event handlers, the dynamic nature of `this` in regular functions often leads to bugs. Arrow functions solve this problem by retaining the `this` value of the surrounding scope.

### Example: Callback with Regular Function

```jsx
function Timer() {
  this.seconds = 0;

  setInterval(function () {
    this.seconds++; // Error: `this` does not refer to Timer's instance
    console.log(this.seconds);
  }, 1000);
}

const timer = new Timer();

```

### Fixed with Arrow Function:

```jsx
function Timer() {
  this.seconds = 0;

  setInterval(() => {
    this.seconds++; // `this` is lexically bound to Timer's instance
    console.log(this.seconds);
  }, 1000);
}

const timer = new Timer();

```

---

### **How Lexical `this` Works in Nested Functions**

Arrow functions are particularly useful in nested functions, as they maintain the `this` of the enclosing scope.

### Example:

```jsx
function Outer() {
  this.value = 42;

  function regularFunction() {
    console.log(this.value); // `this` is dynamic, may not refer to `Outer`
  }

  const arrowFunction = () => {
    console.log(this.value); // `this` is lexically bound to `Outer`
  };

  regularFunction(); // undefined
  arrowFunction();  // 42
}

new Outer();

```

---

### Summary:

- Lexical `this` refers to the `this` value from the scope where the function was **defined**.
- Arrow functions:
    - Do not have their own `this`.
    - Always inherit `this` from the surrounding scope.
- Regular functions:
    - Have their own `this`, determined by the **calling context**.

Arrow functions make working with callbacks, event handlers, and nested functions easier by removing the ambiguity of `this`.

## String

In JavaScript, a string is one of the seven primitive data types. Strings are used to store text data and can be created by enclosing characters in quotes, like "hello".

```jsx
let s1='hell'
let s2='hello'
let s3=`${s1} helloo ${s2}`
console.log(s3)
```

Output:

```jsx
hell helloo hello
```

— The above example demonstrates string interpolation.

### Escape Sequence

JavaScript escape sequences are special characters that begin with a backslash (\) and are used within strings. Here are the common escape sequences:

```jsx
// Common escape sequences
let str = "Line 1\nLine 2";     // \n - newline
let tab = "Column1\tColumn2";    // \t - tab
let quote = "He said \"Hello\""; // \" - double quote
let slash = "C:\\Program Files"; // \\ - backslash
let singleQuote = 'It\'s time';  // \' - single quote
```

Based on the selected code, here's what each line would output:

```jsx
Line 1
Line 2         // Result of "Line 1\nLine 2"

Column1	Column2    // Result of "Column1\tColumn2"

He said "Hello"    // Result of "He said \"Hello\""

C:\Program Files   // Result of "C:\\Program Files"

It's time         // Result of "It\'s time"
```

Each escape sequence produces a special character in the output:

- \n creates a new line
- \t inserts a tab space
- \" allows double quotes within a string
- \\ displays a single backslash
- \' allows single quotes within a string

These escape sequences allow you to include special characters in strings that would otherwise be difficult or impossible to write directly.

### String methods

- toUpperCase()
- toLowerCase()
- startsWith()
- endsWith()
- property: length
- indexOf()
- lastIndexOf()
- slice()
    
    ```jsx
    let name = "hello";
    console.log(name.slice(2, 5));
    ```
    
    The output will be:
    
    ```jsx
    llo
    ```
    
- splice()
- replace()
    
    ```jsx
    let awein = "rain man";
    console.log(awein.replace("man", "woman"));
    ```
    
    The output will be:
    
    ```jsx
    rain woman
    ```
    
- concat()
    
    ```jsx
    let awaam='sm'
    let loves=' for life'
    let con=awaam.concat(loves)
    console.log(con)
    ```
    
    The output will be:
    
    ```jsx
    sm for life
    ```
    

- trim()
    
    ```jsx
    let friend = "     meena     ";
    console.log(friend.trim());
    ```
    
    The output will be:
    
    ```jsx
    meena
    ```
    

— strings are immutable

so,

```jsx
friend[8]='w'
```

this wont work

## Arrays

functions:

- splice() : returns deleted segment.    Syntax: array.splice(startIndex, endIndex, insertitem1, insertitem2……..)
- slice() : returns a  new arrray.
- sort() : sorts the array alphabetically.
    
    to sort in ascending or descending order, use a compare function. 
    
    ```jsx
    let num = [
      44, 2, 89, 3, 11, 1, 90, 32, 5, 8, 445, 64, 23, 12, 34, 56, 78, 9, 0,
    ];
    
    const compare = (a, b) => {
      return a - b;
    };
    num.sort(compare);
    console.log(num);
    ```
    
    The code will sort the array in ascending order and output:
    
    ```jsx
    [ 0, 1, 2, 3, 5, 8, 9, 11, 12, 23, 32, 34, 44, 56, 64, 78, 89, 90, 445 ]
    ```
    
    This is because the compare function `(a, b) => { return a - b }` tells the sort method to arrange numbers in ascending order.
    

- delete property : deletes an item in the array, without altering its length.
    
    ```jsx
    let num1 = [2,4,7,8,3,22]
    console.log(num1.length)
    delete num1[2]
    console.log(num1)
    console.log(num1.length)
    ```
    
    The code will output:
    
    ```jsx
    6           // initial length of array
    [2, 4, empty, 8, 3, 22]  // array after deletion
    6           // length remains unchanged
    ```
    
    This demonstrates that the delete operator removes the element at index 2 (value 7) but leaves an empty slot in the array, keeping the array's length unchanged. The empty slot is sometimes called a "hole" in the array.
    

## Using Loops with Arrays

### For-Each Loop

calls a function for each element of the array.

```jsx
let num2= [2,34,11,874,221,43,22,1,3,4,5,6,7,8,9,10]
num2.forEach((el)=>{
  console.log(el*el)
})
```

The forEach loop will output the square of each number in the array:

```jsx
4
1156
121
763876
48841
1849
484
1
9
16
25
36
49
64
81
100
```

### Array.from

used to create arrays from other objects and HTML collection.

```jsx
let a = document.getElementByClassName("hell");
//it is an HTML collection containing multiple elements
console.log(typeof a)
//a is an object
console.log(Array.from (a));
//created an array from the HTML collection
```

When this code runs, it will:

- Get an HTML collection of elements with class name "hell"
- Log the type of this collection (which will show as "object")
- Convert the HTML collection into an array using Array.from()

### For-in loops with arrays

```jsx
let num3=[12,13,2,3,4,5,6,7,8,9,10]
for(j in num3){
  console.log(j);
}
```

The output will be:

```jsx
0
1
2
3
4
5
6
7
8
9
10
```

This is because for-in loops iterate over the indices (keys) of the array, not the values.

Since array is an object, its keys are its indices.

## Map, Filter and Reduce

Map : creates a new array which can be returned after performing operations on each element of the original array.

```jsx
let num4= [2,34,11,874,221,43,22,1,3,4,5,6]
let num5 = num4.map((el,index)=>{
  return el+index-4;
})
console.log(num5)
```

The output of this code will be a new array where each element is calculated by adding the element's index and subtracting 4 from the original value. Based on the input array [2,34,11,874,221,43,22,1,3,4,5,6], the output will be:

```jsx
[-2, 31, 9, 873, 221, 44, 24, 4, 7, 9, 11, 13]
```

This is because each element (el) is transformed using the formula: el + index - 4

Filter : It returns a new array by filtering the original on basis of a given condition.

```jsx
let num6= [3,2,909,1,3,8,99,0,4,5,6,7,8,9,10]
let num7= num6.filter((el)=>{
  return el>88
})
console.log (num7)
```

Based on the selected code, the output will be:

```jsx
[909, 99]
```

This is because the filter function creates a new array containing only the numbers greater than 88 from the original array.

Reduce : 

Reduce is an array method that takes an array and reduces it to a single value. It processes each element of the array to build a final result.

In this example, reduce takes two arguments:

- A callback function that specifies how to combine the elements
- An initial value (in this case, 0)

The callback function takes two parameters:

- accumulator: stores the running total
- currentValue: the current element being processed

Each time the callback runs, it adds the current value to the accumulator, ultimately producing a single result.

```jsx
let num8=[1,2,3,4,5,6]
let num9= num8.reduce((h1,h2)=>{
  return h1*h2
})
console.log(num9)
```

Let's dry run the reduce function with array [1,2,3,4,5,6]:

Iteration 1: h1 = 1, h2 = 2
Result: 1 * 2 = 2

Iteration 2: h1 = 2, h2 = 3
Result: 2 * 3 = 6

Iteration 3: h1 = 6, h2 = 4
Result: 6 * 4 = 24

Iteration 4: h1 = 24, h2 = 5
Result: 24 * 5 = 120

Iteration 5: h1 = 120, h2 = 6
Result: 120 * 6 = 720

Final output: 720

In this reduce operation, we're multiplying each element with the accumulated result. The function takes two parameters (h1 and h2), where h1 is the accumulator that keeps track of the running product, and h2 is the current element being processed.

### **Spread Operator (`...`) in JavaScript**

The **spread operator** (`...`) allows you to expand elements of an array, object, or other iterable into individual elements. It is useful for combining, copying, or distributing elements of arrays or objects.

---

### **Key Use Cases of the Spread Operator**

1. **Expanding Arrays**:
    - You can use the spread operator to expand elements of an array into individual elements.

### Example:

```jsx
const numbers = [1, 2, 3];
console.log(...numbers); // Output: 1 2 3

```

---

1. **Copying Arrays**:
    - You can create a shallow copy of an array using the spread operator.

### Example:

```jsx
const original = [1, 2, 3];
const copy = [...original];

console.log(copy); // Output: [1, 2, 3]
console.log(original === copy); // Output: false (different references)

```

---

1. **Merging Arrays**:
    - The spread operator is a concise way to merge multiple arrays into one.

### Example:

```jsx
const array1 = [1, 2];
const array2 = [3, 4];
const merged = [...array1, ...array2];

console.log(merged); // Output: [1, 2, 3, 4]

```

---

1. **Spreading Elements into Function Arguments**:
    - The spread operator is useful for passing array elements as arguments to a function.

### Example:

```jsx
const numbers = [1, 2, 3];

function sum(a, b, c) {
  return a + b + c;
}

console.log(sum(...numbers)); // Output: 6

```

---

1. **Copying Objects**:
    - You can create a shallow copy of an object using the spread operator.

### Example:

```jsx
const original = { a: 1, b: 2 };
const copy = { ...original };

console.log(copy); // Output: { a: 1, b: 2 }
console.log(original === copy); // Output: false (different references)

```

---

1. **Merging Objects**:
    - The spread operator allows you to merge multiple objects into one.

### Example:

```jsx
const obj1 = { a: 1, b: 2 };
const obj2 = { c: 3, d: 4 };
const merged = { ...obj1, ...obj2 };

console.log(merged); // Output: { a: 1, b: 2, c: 3, d: 4 }

```

---

1. **Adding or Overriding Properties**:
    - You can use the spread operator to add or override properties in an object.

### Example:

```jsx
const person = { name: "John", age: 30 };
const updated = { ...person, age: 31, city: "New York" };

console.log(updated); // Output: { name: "John", age: 31, city: "New York" }

```

---

1. **Spreading in Arrays or Objects with Rest**:
    - The spread operator works alongside the **rest operator**, which collects the "rest" of the elements.

### Example with Arrays:

```jsx
const numbers = [1, 2, 3, 4, 5];
const [first, second, ...rest] = numbers;

console.log(first); // Output: 1
console.log(second); // Output: 2
console.log(rest);   // Output: [3, 4, 5]

```

### Example with Objects:

```jsx
const person = { name: "John", age: 30, city: "New York" };
const { name, ...details } = person;

console.log(name);    // Output: John
console.log(details); // Output: { age: 30, city: "New York" }

```

---

### **Key Notes**

- **Shallow Copy**:
    - When copying or merging objects/arrays, the spread operator creates a **shallow copy**. For nested objects or arrays, only the outer structure is copied, and inner references remain the same.

### Example:

```jsx
const nested = { a: { b: 1 } };
const shallowCopy = { ...nested };

shallowCopy.a.b = 2;
console.log(nested.a.b); // Output: 2 (inner object is shared)

```

- **Cannot Be Used Directly on Non-Iterables**:
    - The spread operator only works with iterables like arrays, strings, or objects.

---

### **Summary**

The spread operator (`...`) is a powerful and concise tool in JavaScript for:

- Expanding arrays or objects.
- Copying and merging arrays or objects.
- Passing elements as function arguments.

Its versatility makes it a core feature for working with modern JavaScript.

## Event Handling

Events in JavaScript are actions or occurrences that happen during the execution of a program, particularly in response to user interactions. Based on the JavaScript overview from the notes, these events allow you to:

- Add dynamic behavior to web pages
- Handle user interactions in real-time
- Update content dynamically when specific actions occur

Events are a fundamental part of making web pages interactive, as mentioned in the core functionality of JavaScript for web development.

### addEventListener() and removeEventListener()

```jsx
const a = document.getElementByClassName('hello')

let b = function() {
    console.log('wow')
}
    
a.addEventListener('click', b);
let c = prompt('value of c?')
if(c == 2) {
    a.removeEventListener('click', b);
}

// Output:
// 1. When clicking element with class 'hello':
//    "wow" is logged to console (unless c=2)
// 2. When prompted for value of c:
//    if user enters 2, click event listener is removed
//    otherwise, click event listener remains active

if(c==2){
		a.removeEventListener('click',function() {
    console.log('wow')
})}

```

The code won't work because in the second removeEventListener call, a new anonymous function is being passed as the event handler. Even though the function has the same code, it's a different function reference than the original 'b' function that was added.

To remove an event listener, you need to pass the exact same function reference that was used to add it. That's why the first removeEventListener works (using the 'b' reference) but the second one doesn't.

Here's how it should be written instead:

```jsx
if(c == 2) {
    a.removeEventListener('click', b);  // This works because it uses the same function reference
}
```

### Event Object

An Event Object in JavaScript is created whenever an event occurs during program execution, particularly in response to user interactions. Events are crucial for:

- Adding dynamic behavior to web pages
- Handling user interactions in real-time
- Updating content dynamically when specific actions occur

```jsx
let a = (e)=>{console.log(e.target)}

const b = document.getElementById('hell')
b.addEventListener('click', a)
```

Let's break down this code and its execution:

The code sets up a click event listener that logs the target element when clicked. Here's how it works:

1. `let a = (e)=>{console.log(e.target)}` defines a function that takes an event object (e) as parameter and logs the target element of the event
2. `const b = document.getElementById('hell')` gets an HTML element with ID 'hell' and stores it in variable b
3. `b.addEventListener('click', a)` attaches the click event listener to that element

When the element is clicked:

- The event object (e) is automatically created
- The function a is called with this event object
- `e.target` refers to the element that was clicked
- The element will be printed to the console

This code demonstrates how event handling can be used to respond to user interactions in real-timeand update content dynamically.

## Synchronous and Asynchronous Programming

Synchronous programming : 

Synchronous programming is when code executes sequentially, one line at a time in order. Each operation must complete before the next one begins. This means the program "blocks" or waits for each operation to finish before moving on.

For example, when you have multiple lines of code in sequence, each line must finish executing before the next line can begin:

```jsx
let x = 5;
console.log(x);  // This waits for x to be assigned
let y = x + 2;   // This waits for the console.log
console.log(y);  // This waits for y to be calculated
```

In synchronous programming, tasks are completed one after another in a predictable order.

Asynchronous programming : 

Asynchronous programming allows operations to run independently without blocking the execution of other code. Unlike synchronous programming where tasks wait for each other, asynchronous code can continue executing while waiting for other operations to complete.

Key characteristics of asynchronous programming:

- Non-blocking: Code execution continues while waiting for operations to complete
- Parallel execution: Multiple tasks can run simultaneously
- Event-driven: Uses callbacks, promises, and async/await to handle operation completion

This is particularly useful for operations that might take time to complete, such as:

- Fetching data from servers
- Reading files
- Processing large amounts of data

```jsx
console.log("wowoow");
setTimeout(function () {
  console.log("displaying this after 5 seconds");
}, 5000);
console.log("helloooo");
```

The output of this code will be:

```jsx
wowoow
helloooo
displaying this after 5 seconds
```

Here's the dry run explanation:

1. First, "wowoow" is logged immediately
2. Then, setTimeout is encountered, which schedules "displaying this after 5 seconds" to be shown after 5000 milliseconds (5 seconds)
3. Without waiting for setTimeout, "helloooo" is logged next
4. Finally, after 5 seconds have passed, "displaying this after 5 seconds" is displayed

This demonstrates asynchronous programming, where the setTimeout doesn't block the execution of subsequent code while waiting for the timer to complete. Instead of waiting 5 seconds before executing the next line, the program continues running while the timer counts down in the background.

## Callback

A callback is a function that is passed as an argument to another function and is executed after the main function has finished its execution. Callbacks are commonly used in:

- Event handling (like addEventListener)
- Asynchronous operations
- Array methods (like filter, reduce)

For example, in array methods like reduce, the callback function specifies how to combine elements:

```jsx
let numbers = [1,2,3,4,5,6]
numbers.reduce((accumulator, currentValue) => {
    return accumulator * currentValue
})
```

Similarly, in setTimeout, a callback function is used to specify what code should run after the timer completes:

```jsx
setTimeout(function () {
    console.log("This runs after the specified time");
}, 5000);
```

## Callback Hell

When dealing with multiple asynchronous operations that depend on each other, callbacks can lead to deeply nested code structures - this is what's typically known as "callback hell". This can be understood by looking at how asynchronous code works:

In asynchronous programming, operations can run independently without blocking other code execution. For example, when using setTimeout:

```jsx
function f1(callback) {
  setTimeout(() => {
    console.log("Task 1 complete");
    callback();
  }, 2000);
}

function f2(callback) {
  setTimeout(() => {
    console.log("Task 2 complete");
    callback();
  }, 2000);
}
function f3(callback) {
  setTimeout(() => {
    console.log("Task 3 complete");
    callback();
  }, 2000);
}
function f4(callback) {
  setTimeout(() => {
    console.log("Task 4 complete");
    callback();
  }, 2000);
}

f1(() => {
  f2(() => {
    f3(() => {
      f4(() => {
        console.log("All tasks completed");
      });
    });
  });
});

```

Let's dry run the code to understand how it executes:

1. First, f1 is called, which starts a 2-second timer:
- After 2 seconds, prints "Task 1 complete"
- Then calls its callback function, which triggers f2
1. f2 starts another 2-second timer:
- After 2 seconds, prints "Task 2 complete"
- Then calls its callback function, which triggers f3
1. f3 starts another 2-second timer:
- After 2 seconds, prints "Task 3 complete"
- Then calls its callback function, which triggers f4
1. f4 starts the final 2-second timer:
- After 2 seconds, prints "Task 4 complete"
- Then calls its callback which prints "All tasks completed"

Final output (with 2-second gaps between each line):

```
Task 1 complete
Task 2 complete
Task 3 complete
Task 4 complete
All tasks completed
```

Total execution time will be 8 seconds since each task waits for 2 seconds and they run sequentially due to the nested callbacks.

This demonstrates asynchronous execution where code continues running while waiting for operations to complete. When you have multiple such operations depending on each other, it can lead to deeply nested callbacks, creating callback hell.

Modern JavaScript provides better alternatives to handle asynchronous operations, such as Promises and async/await, which help avoid callback hell.

## Promises

In JavaScript, **promises** are objects that represent the eventual completion (or failure) of an asynchronous operation and its resulting value. Promises are used to handle asynchronous code in a more readable and maintainable way, avoiding "callback hell."

### Key Features of Promises:

1. **States of a Promise**:
    - **Pending**: The initial state; the operation is not yet complete.
    - **Fulfilled**: The operation has completed successfully, and the promise has a resolved value.
    - **Rejected**: The operation has failed, and the promise has a reason for the failure (usually an error).
2. **Chaining**: Promises allow chaining of `.then()` methods to sequence operations.

### Creating a Promise:

You can create a promise using the `Promise` constructor, which takes a function with two parameters: `resolve` and `reject`.

```jsx
const myPromise = new Promise((resolve, reject) => {
  let success = true;

  if (success) {
    resolve("Operation was successful!");
  } else {
    reject("Something went wrong.");
  }
});
```

```jsx
function walkdog() {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      let didresolve = true;
      if (didresolve) resolve("walking the dog");
      else reject("You DIDN'T walk the dog");
    }, 1500);
  });
}
function taketrash() {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      let didresolve = true;
      if (didresolve) resolve("taking out the trash");
      else reject("You DIDN'T take out the trash");
    }, 500);
  });
}
function kitchen() {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      let didresolve = true;
      if (didresolve) resolve("cleaning the kitchen");
      else reject("DIDN'T clean the kitchen");
    }, 2500);
  });
}

walkdog()
  .then((value) => {
    console.log(value);
    return kitchen();
  })
  .then((value) => {
    console.log(value);
    return taketrash();
  })
  .then((value) => {
    console.log(value);
    console.log("all tasks finished");
  }).catch(error=> console.error(error));

```

### Code Explanation:

This code defines three asynchronous functions (`walkdog`, `taketrash`, and `kitchen`) that simulate real-world tasks using JavaScript promises. Each function uses `setTimeout` to introduce delays, mimicking asynchronous behavior, and resolves or rejects based on a boolean `didresolve`.

The promises are chained together using `.then()` to ensure the tasks are executed sequentially.

---

### Dry Run (Step-by-Step Execution):

### Step 1: **Call `walkdog()`**

- The `walkdog` function is called.
- Inside the function, a new promise is created, and a `setTimeout` is set for **1500ms**.
- After 1500ms, the `didresolve` variable (set to `true`) causes the promise to resolve with the message `"walking the dog"`.
- This value is passed to the first `.then()`.

### Step 2: **First `.then()`**

- The resolved value `"walking the dog"` is logged to the console:
    
    ```
    walking the dog
    
    ```
    
- The `.then()` returns a call to `kitchen()`.

### Step 3: **Call `kitchen()`**

- The `kitchen` function is executed.
- A new promise is created with a `setTimeout` set for **2500ms**.
- After 2500ms, the promise resolves with the message `"cleaning the kitchen"`.
- This value is passed to the second `.then()`.

### Step 4: **Second `.then()`**

- The resolved value `"cleaning the kitchen"` is logged to the console:
    
    ```
    cleaning the kitchen
    ```
    
- The `.then()` returns a call to `taketrash()`.

### Step 5: **Call `taketrash()`**

- The `taketrash` function is executed.
- A new promise is created with a `setTimeout` set for **500ms**.
- After 500ms, the promise resolves with the message `"taking out the trash"`.
- This value is passed to the third `.then()`.

### Step 6: **Third `.then()`**

- The resolved value `"taking out the trash"` is logged to the console:
    
    ```
    taking out the trash
    ```
    
- The final `console.log("all tasks finished")` is executed:
    
    ```
    all tasks finished
    ```
    

---

### Final Output:

The following is logged to the console in sequence, with delays introduced by the `setTimeout` calls:

```
walking the dog
cleaning the kitchen
taking out the trash
all tasks finished
```

---

### Important Notes:

1. **Sequential Execution**: Each promise runs only after the previous one resolves, thanks to the chained `.then()` calls.
2. **Error Handling**: If any promise is rejected (e.g., setting `didresolve` to `false`), the `.catch()` block will handle the error, logging it to the console and stopping further execution of the chain.
Example of rejection (set `didresolve` to `false` in `kitchen()`):
    
    ```
    walking the dog
    DIDN'T clean the kitchen
    ```
    

## Async/Await

**`async`** and **`await`** are modern JavaScript features introduced in ES2017 (ES8) that simplify working with promises. They allow you to write asynchronous code that looks and behaves like synchronous code, making it easier to read and debug.

---

### **What is `async`?**

- The `async` keyword is used to define a function that always returns a **promise**.
- Inside an `async` function, you can use the `await` keyword to pause the execution of the function until a promise is resolved or rejected.

### **What is `await`?**

- The `await` keyword can only be used inside an `async` function.
- It pauses the execution of the function until the promise is resolved, then returns the resolved value.
- If the promise is rejected, it throws the error, which can be caught using `try...catch`.

---

### Syntax:

```jsx
async function functionName() {
  const result = await somePromise();
  console.log(result);
}

```

---

### Example: Using `async` and `await` with Promises

Let’s rewrite your earlier example using `async` and `await`.

### Original Code (with `.then()`):

```jsx
walkdog()
  .then((value) => {
    console.log(value);
    return kitchen();
  })
  .then((value) => {
    console.log(value);
    return taketrash();
  })
  .then((value) => {
    console.log(value);
    console.log("all tasks finished");
  })
  .catch((error) => console.error(error));

```

### Updated Code (with `async` and `await`):

```jsx
async function performTasks() {
  try {
    const walkDogResult = await walkdog();
    console.log(walkDogResult);

    const kitchenResult = await kitchen();
    console.log(kitchenResult);

    const takeTrashResult = await taketrash();
    console.log(takeTrashResult);

    console.log("all tasks finished");
  } catch (error) {
    console.error(error);
  }
}

performTasks();

```

---

### Explanation of the Updated Code:

1. **`async function performTasks()`**:
    - Declares an asynchronous function that uses `await` to handle promises sequentially.
2. **Using `await`**:
    - `await walkdog()` pauses the function execution until `walkdog` resolves or rejects.
    - If the promise resolves, the result is stored in `walkDogResult` and logged.
    - If the promise rejects, the error is caught in the `catch` block.
3. **Try-Catch for Error Handling**:
    - Wraps the `await` calls to handle errors gracefully.
4. **Readability**:
    - The sequential structure resembles synchronous code, making it easier to understand and maintain.

---

### Output of the Updated Code:

The output remains the same as the `.then()` example:

```
walking the dog
cleaning the kitchen
taking out the trash
all tasks finished

```

---

### Key Points to Remember:

1. **Simplified Promise Handling**:
    - `async/await` avoids deeply nested `.then()` chains.
2. **Sequential vs. Parallel Execution**:
    - Each `await` pauses the execution until the promise resolves, so tasks are executed sequentially.
    - For parallel execution, you can use `Promise.all()`.
    
    Example of parallel execution:
    
    ```jsx
    const [result1, result2, result3] = await Promise.all([
      walkdog(),
      taketrash(),
      kitchen()
    ]);
    console.log(result1, result2, result3);
    
    ```
    
3. **Browser Support**:
    - Widely supported in modern browsers and Node.js.

## Destructuring

**Destructuring** in JavaScript is a convenient way to extract values from arrays or properties from objects and assign them to variables. It simplifies the process of working with complex data structures by providing a concise syntax.

**Destructuring** in JavaScript is a convenient way to extract values from arrays or properties from objects and assign them to variables. It simplifies the process of working with complex data structures by providing a concise syntax.

---

### **Destructuring Arrays**

With arrays, destructuring assigns values to variables based on their position in the array.

### Syntax:

```jsx
const [var1, var2, ...rest] = array;

```

### Example:

```jsx
const numbers = [1, 2, 3, 4, 5];

const [first, second] = numbers;
console.log(first);  // Output: 1
console.log(second); // Output: 2

// Using rest operator to collect remaining values
const [one, two, ...others] = numbers;
console.log(others); // Output: [3, 4, 5]

```

---

### **Destructuring Objects**

With objects, destructuring assigns values to variables based on **matching property names**.

### Syntax:

```jsx
const { prop1, prop2, ...rest } = object;

```

### Example:

```jsx
const user = {
  name: "John",
  age: 30,
  location: "New York"
};

const { name, age } = user;
console.log(name); // Output: John
console.log(age);  // Output: 30

// Using rest operator to collect remaining properties
const { location, ...details } = user;
console.log(details); // Output: { name: "John", age: 30 }

```

---

### **Default Values**

You can assign default values when destructuring to handle missing values.

### Example:

```jsx
const { name, age, country = "USA" } = { name: "John", age: 30 };
console.log(country); // Output: USA

```

---

### **Renaming Variables**

You can rename variables while destructuring objects.

### Example:

```jsx
const user = { name: "John", age: 30 };
const { name: userName, age: userAge } = user;

console.log(userName); // Output: John
console.log(userAge);  // Output: 30

```

---

### **Nested Destructuring**

You can destructure nested objects or arrays.

### Objects:

```jsx
const person = {
  name: "Alice",
  address: {
    city: "Paris",
    zip: 75000
  }
};

const { address: { city, zip } } = person;
console.log(city); // Output: Paris
console.log(zip);  // Output: 75000

```

### Arrays:

```jsx
const colors = [["red", "green"], ["blue", "yellow"]];

const [[primary1, primary2], [secondary1, secondary2]] = colors;
console.log(primary1); // Output: red
console.log(secondary1); // Output: blue

```

---

### **Destructuring in Function Parameters**

You can use destructuring to directly extract values from arguments passed to a function.

### Example:

```jsx
function greet({ name, age }) {
  console.log(`Hello, ${name}. You are ${age} years old.`);
}

const user = { name: "John", age: 30 };
greet(user); // Output: Hello, John. You are 30 years old.

```

---

### **Key Advantages of Destructuring:**

1. Simplifies code by avoiding repetitive property access or index access.
2. Makes it easier to work with nested or complex data structures.
3. Enables concise and clean handling of function parameters.

---

---

# Source: Advanced JavaScript Technical Interview Masterclass

# Advanced JavaScript: Technical Interview Masterclass Notes

1. The Foundation: Execution Context and the JavaScript Runtime

Understanding
 the JavaScript Runtime Environment (JRE) is the non-negotiable first 
step for any senior-level developer. While juniors focus on syntax, 
architects must understand the underlying mechanics to diagnose 
performance bottlenecks and memory leaks. The strategic takeaway for a 
senior engineer is that the **Main Thread** is shared between the Call Stack and the **Render Pipe**. If the stack is not empty, the browser cannot paint, leading to "jank" or a frozen UI.

The Components of Runtime

The JRE is an orchestration of four essential components:

- **The JavaScript Engine:** Consists of the **Memory Heap**, where memory is allocated for variables and functions, and the **Call Stack**, where the engine tracks execution.
- **Web APIs:** Features like `setTimeout`, `fetch`, and DOM events provided by the browser environment (or Node.js), not the language itself.
- **Callback/Task Queue:** A First-In, First-Out (FIFO) queue for callbacks from Web APIs waiting for execution.
- **The Event Loop:** The coordinator that manages the flow between the Call Stack and the various queues.

Execution Mechanics

JavaScript is inherently **synchronous, blocki ng, and single-threaded**. It utilizes a **Call Stack** operating on a **Last In, First Out (LIFO)**
 basis. When a function is invoked, it is pushed onto the stack; it is 
only popped off when it returns a value or completes its execution.

Predict Stack Behavior

Analyze the following execution flow to predict stack behavior:

```
console.log('First');
console.log('Second');
console.log('Third');
```

1. **Global Execution Context** is pushed onto the stack.
2. `console.log('First')` is pushed, executes (printing "First"), and is popped.
3. `console.log('Second')` is pushed, executes (printing "Second"), and is popped.
4. `console.log('Third')` is pushed, executes (printing "Third"), and is popped.
5. The file ends; the Global Context is popped.

**Connective Tissue:**
 While the stack handles the "when" of execution, JavaScript uses 
Lexical Scoping to handle the "where" of variable accessibility, leading
 to the phenomenon of Hoisting.

--------------------------------------------------------------------------------

2. Lexical Scoping and the Mechanics of Hoisting

JavaScript determines variable visibility via Lexical Scoping, established during the **Creation Phase** of the execution context. This is the stage where the engine scans for declarations before any code is executed.

Lexical Scoping Analysis

Variable lookup follows a strict, uni-directional path: it moves **up** the scope chain but never **down**. Using the source example of variables a=10 (Global), b=20 (Outer), and c=30 (Inner):

- To find **c**: Found immediately in the **Innermost Function Scope**.
- To find **b**: Not in `inner()`; the engine moves up to the **Outer Function Scope**.
- To find **a**: Not in `inner()` or `outer()`; the engine moves up to the **Global Scope**.

Synthesizing Hoisting

Hoisting is a byproduct of the Creation Phase. **Function declarations**
 are hoisted with their full definition, allowing them to be called 
before they appear in the code. Variables behave differently: while the 
engine "recognizes" them, `let` and `const` respect **block scope** (curly braces), whereas `var` respects **function scope**. Attempting to access `let` or `const` variables before declaration results in a Temporal Dead Zone error, despite the engine being aware of their existence.

**Connective Tissue:**
 When a function is returned from another and "remembers" its lexical 
environment—even after the parent's execution context is popped off the 
stack—we have a Closure.

--------------------------------------------------------------------------------

3. Deep Dive: Closures and Persistent Memory

A closure is the combination of a function bundled together with 
references to its surrounding state. In a technical sense, it provides a
 function with **Persistent Memory**.

Core Implementation: The Counter Analysis

```
function outer() {
    let counter = 0;
    function inner() {
        counter++;
        console.log(counter);
    }
    return inner;
}

const fn = outer();
fn(); // Logs: 1
fn(); // Logs: 2
```

Analytical Comparison

- **Calling outer() twice:** Calling `outer(); outer();` creates two distinct, temporary memory allocations. Each returns `1` because the internal `counter` is re-initialized to `0` each time.
- **Calling the returned function fn() twice:** When `outer()` returns `inner`, it doesn't just return code; it returns a "bundle" of the function and its scope chain. The `counter` variable persists in memory, allowing the state to increment to `2` on the second call.

**Connective Tissue:** Closures are the foundation of **Currying**, a functional programming pattern where a function f(a,b,c) is transformed into a series of nesting functions f(a)(b)(c), allowing for reusable, partially applied functions.

--------------------------------------------------------------------------------

4. Asynchronous JavaScript: From Callbacks to Promises

The
 shift from callbacks to Promises was driven by the need for 
maintainability and the elimination of "Callback Hell"—the deeply 
nested, unreadable structure of dependent async operations.

Timers and the Web API Layer

`setTimeout` and `setInterval` are not part of the JavaScript language; they are **Web APIs**. They allow the engine to offload tasks to the browser, preventing the single-threaded Call Stack from blocking.

The Promise Solution: The Taco Truck Analogy

A Promise is a proxy for a value that is currently unknown but will be settled later.

- **Pending:** The initial state (e.g., waiting for your friend to reach the taco truck).
- **Fulfilled:** The operation succeeded (e.g., "I got the tacos").
- **Rejected:** The operation failed (e.g., "The truck is closed").

Advanced Promise Static Methods

| Method | Input Requirement | Settlement Behavior |
| --- | --- | --- |
| **Promise.all** | Array of promises | Fails fast: Rejects if **any** promise fails; resolves only if all succeed. |
| **Promise.allSettled** | Array of promises | Returns an **array of objects** describing the outcome (`status` and `value`/`reason`) for every promise. |
| **Promise.race** | Array of promises | Settles (resolves or rejects) as soon as the **first** promise in the array settles. |

**Connective Tissue:** While Promises provide a cleaner structure, **Async/Await** (ES2017) provides the "syntactical sugar" needed to write asynchronous code that reads like synchronous logic.

--------------------------------------------------------------------------------

5. Mastering Async/Await and Concurrency Patterns

The `async/await` keywords do not change the underlying Promise-based model; they simply improve the developer experience.

The Async Keyword

An `async`
 function always returns a Promise. If the code does not explicitly 
return a promise, the engine automatically wraps the returned value in a
 resolved promise.

The Await Operator

`await` suspends the execution of the local `async` function until the promise settles. Crucially, it does **not** block the main thread; the engine is free to handle other tasks (like UI updates) while the function is suspended.

Evaluating Execution Patterns

- **Sequential:** `await taskA(); await taskB();` — Total time = sum of both. Use only if B depends on A.
- **Concurrent:** `const a = taskA(); const b = taskB(); await a; await b;` — Fire both tasks into the Web API layer simultaneously. Total time = duration of the longest task.
- **Parallel:** `Promise.all([taskA(), taskB()])` — Executes multiple async functions independently and waits for all to settle.

**Connective Tissue:**
 Despite the synchronous appearance, the timing of these operations is 
strictly governed by the priority levels of the Event Loop.

--------------------------------------------------------------------------------

6. The Event Loop: Task Queues vs. Microtask Queues

The Event Loop is the "Brain" of the JRE. It prioritizes different types of asynchronous callbacks using two distinct queues.

The Execution Algorithm

The Event Loop follows a prioritized 3-step loop:

1. **Check Call Stack:** If any function is currently on the stack, the loop waits.
2. **Process Microtask Queue (High Priority):** Empty the **entire** Microtask Queue (Promises, `process.nextTick`). Note: If a microtask adds another microtask, the loop will stay here, potentially **starving** the Task Queue.
3. **Process Task Queue (Low Priority):** Process **one** item from the Task/Callback Queue (`setTimeout`, `setInterval`).

The "Grand Finale" Execution Order

Analyze the following scenario: A `setTimeout(0)`, a `Promise.resolve()`, and a `while` loop that blocks for 3 seconds. The execution order is:

1. **Synchronous code:** Includes the `while` loop and any trailing `console.logs`. (Result: `"second"`).
2. **Microtasks:** The Promise callback. (Result: `"Promise value"`).
3. **Tasks:** The `setTimeout` callback. (Result: `"first"`).

**The "Zero Delay" Paradox:** `setTimeout(..., 0)` is a **minimum delay**,
 not a guarantee. It must wait for the Call Stack to be empty AND the 
entire Microtask Queue to be cleared before it can execute.

--------------------------------------------------------------------------------

7. Interview Quick-Reference Summary

| Concept | Key Technical Takeaway | Interview "Gotcha" to Mention |
| --- | --- | --- |
| **Execution Context** | Single-threaded LIFO stack shared with the Render Pipe. | Heavy stack usage blocks the browser from painting/rendering. |
| **Hoisting** | Declarations are mapped in the Creation Phase. | `let/const` are hoisted but inaccessible (TDZ); `var` is function-scoped. |
| **Closures** | Functions bundled with their lexical environment (Persistent Memory). | **Stale Closures** in React hooks or long-running event listeners. |
| **Event Loop** | Orchestrates the Stack, Microtask Queue, and Task Queue. | Microtasks have absolute priority; `setTimeout(0)` is a minimum delay. |
| **Promises** | Objects representing eventual settlement (Pending/Fulfilled/Rejected). | `Promise.all` fails fast; `allSettled` returns status objects for all. |

Mastering
 these internals transforms a developer from a language user into an 
architect, capable of building high-performance, non-blocking 
applications that respect the constraints of the JavaScript platform. 
#H1
