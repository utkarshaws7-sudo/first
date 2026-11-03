# 🚀 JavaScript (JS) – Complete Notes

## 📌 1. Introduction to JavaScript

JavaScript is a high-level, interpreted programming language used to build dynamic and interactive web applications.

### Features
- Lightweight and dynamically typed.
- Single-threaded with asynchronous capabilities.
- Prototype-based object-oriented programming.
- Supports functional and event-driven programming.
- Runs in browsers and server-side environments using Node.js.

---

## 📦 2. Variables

JavaScript provides three ways to declare variables:

```javascript
var name = "Utkarsh";
let age = 22;
const country = "India";
```

| Keyword | Scope | Reassignable | Redeclarable |
|---|---|---|---|
| `var` | Function | Yes | Yes |
| `let` | Block | Yes | No |
| `const` | Block | No | No |

**Best Practice:** Prefer `const` by default and use `let` when reassignment is required. Avoid `var` in modern JavaScript.

---

## 🔢 3. Data Types

### Primitive Data Types

1. String
2. Number
3. Boolean
4. Undefined
5. Null
6. BigInt
7. Symbol

```javascript
let name = "Utkarsh";
let age = 22;
let isDeveloper = true;
let value;
let data = null;
let bigNumber = 12345678901234567890n;
let uniqueId = Symbol("id");
```

### Non-Primitive Data Types

- Object
- Array
- Function

```javascript
const user = {
    name: "Utkarsh",
    age: 22
};

const skills = ["JavaScript", "React", "Node.js"];
```

---

## ➕ 4. Operators

### Arithmetic Operators

```javascript
let a = 10;
let b = 5;

console.log(a + b); // 15
console.log(a - b); // 5
console.log(a * b); // 50
console.log(a / b); // 2
console.log(a % b); // 0
console.log(a ** b); // 100000
```

### Comparison Operators

```javascript
10 == "10";  // true
10 === "10"; // false
10 != "10";  // false
10 !== "10"; // true
10 > 5;      // true
10 <= 5;     // false
```

### Logical Operators

```javascript
true && false; // false
true || false; // true
!true;         // false
```

---

## 🔀 5. Conditional Statements

### If-Else

```javascript
let age = 20;

if (age >= 18) {
    console.log("Adult");
} else {
    console.log("Minor");
}
```

### Ternary Operator

```javascript
let result = age >= 18 ? "Adult" : "Minor";
```

### Switch Statement

```javascript
let day = 2;

switch (day) {
    case 1:
        console.log("Monday");
        break;
    case 2:
        console.log("Tuesday");
        break;
    default:
        console.log("Invalid day");
}
```

---

## 🔁 6. Loops

### For Loop

```javascript
for (let i = 0; i < 5; i++) {
    console.log(i);
}
```

### While Loop

```javascript
let i = 0;

while (i < 5) {
    console.log(i);
    i++;
}
```

### Do-While Loop

```javascript
let i = 0;

do {
    console.log(i);
    i++;
} while (i < 5);
```

### For-Of Loop

Used to iterate over iterable values.

```javascript
const arr = [10, 20, 30];

for (const value of arr) {
    console.log(value);
}
```

### For-In Loop

Used to iterate over enumerable object keys.

```javascript
const user = { name: "Utkarsh", age: 22 };

for (const key in user) {
    console.log(key, user[key]);
}
```

---

## ⚙️ 7. Functions

Functions are reusable blocks of code.

### Function Declaration

```javascript
function add(a, b) {
    return a + b;
}

console.log(add(10, 20));
```

### Function Expression

```javascript
const multiply = function(a, b) {
    return a * b;
};
```

### Arrow Function

```javascript
const subtract = (a, b) => a - b;
```

### Default Parameters

```javascript
function greet(name = "Guest") {
    return `Hello ${name}`;
}
```

### Rest Parameters

```javascript
function sum(...numbers) {
    return numbers.reduce((total, num) => total + num, 0);
}
```

### Callback Function

A function passed as an argument to another function.

```javascript
function greet(name, callback) {
    console.log("Hello " + name);
    callback();
}

greet("Utkarsh", () => {
    console.log("Welcome!");
});
```

---

## 📚 8. Arrays

Arrays store multiple values in a single variable.

```javascript
const numbers = [10, 20, 30, 40];
```

### Common Array Methods

| Method | Description |
|---|---|
| `push()` | Add element at end |
| `pop()` | Remove element from end |
| `shift()` | Remove first element |
| `unshift()` | Add element at beginning |
| `slice()` | Extract a portion |
| `splice()` | Add/remove elements |
| `includes()` | Check if element exists |
| `indexOf()` | Find element index |
| `join()` | Convert array to string |
| `reverse()` | Reverse array |
| `sort()` | Sort array |

### Important Higher-Order Methods

**map()**

Returns a new array after transforming each element.

```javascript
const nums = [1, 2, 3];

const result = nums.map(num => num * 2);

// [2, 4, 6]
```

**filter()**

Returns elements that satisfy a condition.

```javascript
const nums = [1, 2, 3, 4, 5];

const result = nums.filter(num => num % 2 === 0);

// [2, 4]
```

**reduce()**

Reduces an array to a single value.

```javascript
const nums = [1, 2, 3, 4];

const sum = nums.reduce((acc, curr) => acc + curr, 0);

// 10
```

**find()**

Returns the first matching element.

```javascript
const nums = [10, 20, 30];

const result = nums.find(num => num > 15);

// 20
```

**some() and every()**

```javascript
const nums = [2, 4, 6];

nums.some(num => num > 5);  // true
nums.every(num => num % 2 === 0); // true
```

---

## 🧱 9. Objects

Objects store data in key-value pairs.

```javascript
const user = {
    name: "Utkarsh",
    age: 22,
    role: "Developer",

    greet() {
        console.log("Hello!");
    }
};

console.log(user.name);
console.log(user["age"]);

user.greet();
```

### Object Destructuring

```javascript
const { name, age } = user;
```

### Spread Operator

```javascript
const userCopy = { ...user };
```

### Object Methods

```javascript
Object.keys(user);
Object.values(user);
Object.entries(user);
Object.assign({}, user);
Object.hasOwn(user, "name");
```

---

## 🔗 10. Spread and Rest Operators

### Spread Operator

Expands iterable elements or object properties.

```javascript
const arr1 = [1, 2, 3];
const arr2 = [...arr1, 4, 5];

const user1 = { name: "Utkarsh" };
const user2 = { ...user1, age: 22 };
```

### Rest Operator

Collects multiple values into an array.

```javascript
function calculate(...numbers) {
    return numbers.reduce((a, b) => a + b, 0);
}
```

---

## 🔤 11. Strings

```javascript
let str = "JavaScript Developer";
```

### Common String Methods

```javascript
str.length;
str.toUpperCase();
str.toLowerCase();
str.trim();
str.includes("JavaScript");
str.startsWith("Java");
str.endsWith("Developer");
str.indexOf("Script");
str.slice(0, 10);
str.replace("Developer", "Engineer");
str.split(" ");
```

### Template Literals

```javascript
const name = "Utkarsh";

console.log(`Hello, ${name}!`);
```

---

## 🌐 12. DOM Manipulation

DOM stands for Document Object Model. It allows JavaScript to interact with HTML elements.

### Selecting Elements

```javascript
document.getElementById("heading");
document.querySelector(".container");
document.querySelectorAll("p");
document.getElementsByClassName("box");
document.getElementsByTagName("div");
```

### Modifying Elements

```javascript
const heading = document.querySelector("h1");

heading.textContent = "Hello JavaScript";
heading.style.color = "blue";
heading.innerHTML = "<span>Hello</span>";
```

### Creating Elements

```javascript
const div = document.createElement("div");

div.textContent = "New Element";

document.body.appendChild(div);
```

### Removing Elements

```javascript
const element = document.querySelector(".box");

element.remove();
```

---

## 🖱️ 13. Events

Events allow JavaScript to respond to user interactions.

```javascript
const button = document.querySelector("button");

button.addEventListener("click", () => {
    console.log("Button clicked!");
});
```

### Common Events

- `click`
- `dblclick`
- `mouseover`
- `mouseout`
- `keydown`
- `keyup`
- `submit`
- `change`
- `input`
- `load`

### Event Object

```javascript
button.addEventListener("click", (event) => {
    console.log(event.target);
    console.log(event.type);
});
```

---

## ⏳ 14. Asynchronous JavaScript

JavaScript supports asynchronous operations through callbacks, Promises, and async/await.

### setTimeout()

```javascript
setTimeout(() => {
    console.log("Executed after 2 seconds");
}, 2000);
```

### setInterval()

```javascript
setInterval(() => {
    console.log("Repeated every second");
}, 1000);
```

### Promises

A Promise represents the eventual completion or failure of an asynchronous operation.

```javascript
const promise = new Promise((resolve, reject) => {
    const success = true;

    if (success) {
        resolve("Operation successful");
    } else {
        reject("Operation failed");
    }
});

promise
    .then(result => console.log(result))
    .catch(error => console.log(error))
    .finally(() => console.log("Completed"));
```

### Async/Await

```javascript
async function getData() {
    try {
        const response = await fetch("https://jsonplaceholder.typicode.com/users");

        if (!response.ok) {
            throw new Error("Request failed");
        }

        const data = await response.json();

        console.log(data);
    } catch (error) {
        console.log(error.message);
    }
}

getData();
```

### Promise Methods

```javascript
Promise.all([]);
Promise.allSettled([]);
Promise.race([]);
Promise.any([]);
```

---

## 📡 15. Fetch API

Fetch API is used to make HTTP requests.

### GET Request

```javascript
async function getUsers() {
    const response = await fetch("/api/users");
    const data = await response.json();

    return data;
}
```

### POST Request

```javascript
async function createUser() {
    const response = await fetch("/api/users", {
        method: "POST",

        headers: {
            "Content-Type": "application/json"
        },

        body: JSON.stringify({
            name: "Utkarsh",
            age: 22
        })
    });

    return await response.json();
}
```

---

## 🏗️ 16. Object-Oriented Programming (OOP)

### Classes

```javascript
class Person {
    constructor(name, age) {
        this.name = name;
        this.age = age;
    }

    greet() {
        console.log(`Hello ${this.name}`);
    }
}

const person = new Person("Utkarsh", 22);

person.greet();
```

### Inheritance

```javascript
class Developer extends Person {
    constructor(name, age, skill) {
        super(name, age);
        this.skill = skill;
    }

    showSkill() {
        console.log(this.skill);
    }
}
```

### Encapsulation

```javascript
class BankAccount {
    #balance = 0;

    deposit(amount) {
        this.#balance += amount;
    }

    getBalance() {
        return this.#balance;
    }
}
```

---

## 🧠 17. Advanced JavaScript Concepts

Important concepts for interviews and real-world development:

1. Execution Context
2. Call Stack
3. Hoisting
4. Temporal Dead Zone (TDZ)
5. Scope and Scope Chain
6. Closures
7. Lexical Environment
8. `this` Keyword
9. Call, Apply and Bind
10. Prototypes and Prototypal Inheritance
11. Event Loop
12. Microtask Queue
13. Macrotask Queue
14. Debouncing
15. Throttling
16. Currying
17. Memoization
18. Shallow Copy vs Deep Copy
19. Garbage Collection
20. Event Delegation

### Closure Example

```javascript
function outer() {
    let count = 0;

    return function inner() {
        count++;
        return count;
    };
}

const counter = outer();

console.log(counter()); // 1
console.log(counter()); // 2
console.log(counter()); // 3
```

### Debouncing Example

```javascript
function debounce(callback, delay) {
    let timer;

    return function (...args) {
        clearTimeout(timer);

        timer = setTimeout(() => {
            callback.apply(this, args);
        }, delay);
    };
}
```

---

## 📦 18. ES6+ Features

Modern JavaScript features:

- `let` and `const`
- Arrow Functions
- Template Literals
- Destructuring
- Spread and Rest Operators
- Default Parameters
- Classes
- Modules
- Promises
- Optional Chaining
- Nullish Coalescing
- Dynamic Imports

### Optional Chaining

```javascript
const user = {};

console.log(user?.address?.city);
```

### Nullish Coalescing

```javascript
const username = null;

console.log(username ?? "Guest");
```

### ES Modules

```javascript
// math.js
export const add = (a, b) => a + b;

// app.js
import { add } from "./math.js";

console.log(add(10, 20));
```

---

## 🛠️ 19. Error Handling

```javascript
try {
    const result = someFunction();
    console.log(result);
} catch (error) {
    console.log(error.message);
} finally {
    console.log("Execution completed");
}
```

### Throwing Custom Errors

```javascript
function validateAge(age) {
    if (age < 18) {
        throw new Error("Age must be 18 or above");
    }

    return true;
}
```

---

## 💾 20. Storage in Browser

### Local Storage

Data persists until explicitly removed.

```javascript
localStorage.setItem("name", "Utkarsh");

const name = localStorage.getItem("name");

localStorage.removeItem("name");

localStorage.clear();
```

### Session Storage

Data persists for the current browser tab session.

```javascript
sessionStorage.setItem("token", "12345");

sessionStorage.getItem("token");
```

---

## 📋 21. Useful JavaScript Concepts for Interviews

| Concept | Importance |
|---|---|
| `==` vs `===` | High |
| `var` vs `let` vs `const` | High |
| Hoisting | High |
| Closures | High |
| Event Loop | High |
| Promises | High |
| Async/Await | High |
| `this` keyword | High |
| Prototypes | High |
| Debouncing | High |
| Throttling | High |
| Map, Filter, Reduce | High |
| Shallow vs Deep Copy | High |
| Call, Apply, Bind | High |
| Event Delegation | Medium |

---

## 🎯 22. JavaScript Practice Questions

### Beginner
- Reverse a string.
- Check whether a number is prime.
- Find the largest element in an array.
- Remove duplicates from an array.
- Check whether a string is a palindrome.

### Intermediate
- Flatten a nested array.
- Find the frequency of elements.
- Implement debounce.
- Implement throttle.
- Group objects by a property.
- Find the intersection of two arrays.

### Advanced
- Implement `Promise.all()`.
- Implement a custom `map()` function.
- Implement a custom `filter()` function.
- Implement a custom `reduce()` function.
- Implement memoization.
- Implement deep cloning.
- Implement a basic event emitter.

---

## 🔗 23. Useful Resources

- [MDN JavaScript Documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
- [JavaScript.info](https://javascript.info/)
- [ECMAScript Documentation](https://tc39.es/ecma262/)
- [Node.js Documentation](https://nodejs.org/docs/latest/api/)

---

## ⭐ Conclusion

JavaScript is one of the most important technologies in modern web development.

To become proficient, focus on:

1. Mastering fundamentals.
2. Understanding asynchronous JavaScript.
3. Learning advanced concepts.
4. Practicing coding problems.
5. Building real-world projects.

**Happy Coding! 🚀**
