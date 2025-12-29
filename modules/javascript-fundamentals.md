<div align="center">
  <a href="https://vetswhocode.io">
    <img src="../img/vwc-logo.png" alt="Vets Who Code" width="400px" />
  </a>
</div>

<h1 align="center">Module 5: JavaScript — Unlocking Web Interactivity</h1>

**⏱ Estimated Time: 10-14 hours**

---

## Why This Matters

HTML gives you structure. CSS gives you style. JavaScript gives you **behavior**.

JavaScript makes web pages interactive. It responds to clicks, validates forms, updates content without refreshing, and powers everything from simple animations to complex applications.

This is where you become a programmer.

---

## How to Learn JavaScript

The best way to learn programming is by writing programs. This module has explanations, but the real learning happens when you write the code yourself.

For every concept:

1. Read the explanation
2. Type the examples yourself (don't copy-paste)
3. Experiment—change things and see what happens
4. Complete the exercises

When you get stuck, that's not failure. That's learning. Work through it.

---

## Preparing Your Toolkit

Before we embark on our JavaScript journey, make sure you have the following tools:

1. **Text Editor:** Think of it as your coding canvas. VS Code (which you set up in Module 2).
2. **Web Browser:** Your window into the web. Chrome, Firefox, or Edge will be your stage.

---

## Running JavaScript

### In the Browser Console

1. Open any web page
2. Right-click → Inspect (or F12)
3. Click the "Console" tab
4. Type JavaScript and press Enter

Try it:

```javascript
console.log("Hello, World!");
```

### In an HTML File

```html
<!DOCTYPE html>
<html>
<head>
  <title>My First JavaScript Code</title>
</head>
<body>
  <h1>Check the console</h1>
  <button onclick="showMessage()">Click me</button>
  <p id="message"></p>

  <script>
    function showMessage() {
      document.getElementById("message").innerHTML = "Hello, World!";
    }
    console.log("Hello from the script!");
  </script>
</body>
</html>
```

### External JavaScript File (Recommended)

```html
<body>
  <h1>My Page</h1>

  <script src="script.js"></script>
</body>
```

Put the `<script>` tag at the end of `<body>` so HTML loads first.

You can also keep your JavaScript code in separate files and link them to your HTML using the `<script>` tag. This keeps your code organized and easy to manage.

---

## Variables

Variables store values so you can use them later.

### Declaration

```javascript
let name = "Jerome";
let age = 30;
let isVeteran = true;
```

### let vs const vs var

**let** — Value can change:
```javascript
let score = 0;
score = 10;      // OK
score = score + 5; // OK
```

**const** — Value cannot be reassigned:
```javascript
const PI = 3.14159;
PI = 3;          // ERROR!
```

**var** — Old way (avoid in modern code):
```javascript
var name = "John";
```

Use `const` by default. Use `let` when you need to reassign.

### Naming Rules

- Must start with a letter, `_`, or `$`
- Can contain letters, numbers, `_`, `$`
- Case sensitive (`name` and `Name` are different)
- Use camelCase: `firstName`, `isLoggedIn`, `totalAmount`

---

## Data Types

### Primitive Types

```javascript
// String — text
let greeting = "Hello";
let name = 'Jerome';
let message = `Welcome, ${name}!`; // Template literal

// Number — integers and decimals
let count = 42;
let price = 19.99;
let age = 25;
const pi = 3.14;

// Boolean — true or false
let isActive = true;
let hasAccount = false;

// Undefined — declared but no value
let something;
console.log(something); // undefined

// Null — intentionally empty
let empty = null;
```

### Checking Types

```javascript
typeof "hello"    // "string"
typeof 42         // "number"
typeof true       // "boolean"
typeof undefined  // "undefined"
typeof null       // "object" (this is a JavaScript quirk)
```

---

## Operators

### Arithmetic

```javascript
let a = 10;
let b = 3;
let x = 5;
let y = 10;

a + b    // 13 — Addition
a - b    // 7  — Subtraction
a * b    // 30 — Multiplication
a / b    // 3.333... — Division
a % b    // 1  — Remainder (modulo)
a ** b   // 1000 — Exponent

let sum = x + y; // 15
let difference = y - x; // 5
let product = x * y; // 50
let quotient = y / x; // 2
```

### Assignment

```javascript
let x = 10;
x += 5;   // x = x + 5 → 15
x -= 3;   // x = x - 3 → 12
x *= 2;   // x = x * 2 → 24
x /= 4;   // x = x / 4 → 6
x++;      // x = x + 1 → 7
x--;      // x = x - 1 → 6
```

### Comparison

```javascript
5 == "5"    // true — Equal (loose, converts types)
5 === "5"   // false — Strict equal (no conversion)
5 != "5"    // false — Not equal (loose)
5 !== "5"   // true — Strict not equal

10 > 5      // true
10 < 5      // false
10 >= 10    // true
10 <= 9     // false
```

**Always use `===` and `!==`** to avoid type conversion surprises.

### Logical

```javascript
true && true    // true — AND (both must be true)
true && false   // false
true || false   // true — OR (one must be true)
false || false  // false
!true           // false — NOT (flips the value)
!false          // true
```

---

## Strings

### Creating Strings

```javascript
let single = 'Hello';
let double = "World";
let template = `Hello, ${name}!`;  // Can include variables
let greeting = "Hello, world!";
let name = "Alice";
```

### String Properties and Methods

```javascript
let text = "Hello, World!";
let message = "Hello, world!";

text.length                // 13
text.toUpperCase()         // "HELLO, WORLD!"
text.toLowerCase()         // "hello, world!"
text.indexOf("World")      // 7 (position where "World" starts)
text.includes("Hello")     // true
text.startsWith("Hello")   // true
text.endsWith("!")         // true
text.slice(0, 5)           // "Hello" (from index 0 to 4)
text.slice(7)              // "World!" (from index 7 to end)
text.replace("World", "JavaScript")  // "Hello, JavaScript!"
text.split(", ")           // ["Hello", "World!"]
text.trim()                // Removes whitespace from ends

message.length             // 13
message.toUpperCase()      // "HELLO, WORLD!"
message.indexOf("world")   // 7
```

### Template Literals

```javascript
let name = "Jerome";
let age = 30;

// Old way (concatenation)
let message = "Hello, " + name + "! You are " + age + " years old.";

// New way (template literals)
let message = `Hello, ${name}! You are ${age} years old.`;

// Multi-line strings
let html = `
  <div class="card">
    <h2>${name}</h2>
    <p>Age: ${age}</p>
  </div>
`;
```

---

## Control Flow

### if / else

```javascript
let age = 20;
let score = 85;

if (age >= 21) {
  console.log("You can enter.");
} else if (age >= 18) {
  console.log("You can enter but cannot drink.");
} else {
  console.log("You cannot enter.");
}

if (score >= 90) {
  console.log("A Grade");
} else if (score >= 80) {
  console.log("B Grade");
} else {
  console.log("C or Lower");
}
```

### Ternary Operator

Short form for simple if/else:

```javascript
let status = age >= 18 ? "adult" : "minor";
```

### switch

```javascript
let day = "Monday";

switch (day) {
  case "Monday":
    console.log("Start of the week");
    break;
  case "Friday":
    console.log("Almost weekend!");
    break;
  case "Saturday":
  case "Sunday":
    console.log("Weekend!");
    break;
  default:
    console.log("Regular day");
}
```

Don't forget `break` or execution falls through to the next case.

---

## Loops

### for Loop

```javascript
for (let i = 0; i < 5; i++) {
  console.log(i);  // 0, 1, 2, 3, 4
  console.log("Count: " + i);
}
```

Parts: `for (initialization; condition; update)`

### while Loop

```javascript
let count = 0;

while (count < 5) {
  console.log(count);
  count++;
}

let count = 0;
while (count < 3) {
  console.log("Looping...");
  count++;
}
```

### for...of Loop

Iterates over array elements:

```javascript
let colors = ["red", "green", "blue"];

for (let color of colors) {
  console.log(color);  // red, green, blue
}
```

### for...in Loop

Iterates over object keys:

```javascript
let person = { name: "Jerome", age: 30 };

for (let key in person) {
  console.log(key, person[key]);  // name Jerome, age 30
}
```

### Loop Control

```javascript
// break — exit the loop entirely
for (let i = 0; i < 10; i++) {
  if (i === 5) break;
  console.log(i);  // 0, 1, 2, 3, 4
}

// continue — skip to next iteration
for (let i = 0; i < 5; i++) {
  if (i === 2) continue;
  console.log(i);  // 0, 1, 3, 4
}
```

---

## Functions

Functions are reusable blocks of code.

### Function Declaration

```javascript
function greet(name) {
  return `Hello, ${name}!`;
}

let message = greet("Jerome");  // "Hello, Jerome!"

function greet(name) {
  console.log("Hello, " + name + "!");
}

greet("Alice");
```

### Function Expression

```javascript
const greet = function(name) {
  return `Hello, ${name}!`;
};
```

### Arrow Functions

Modern, shorter syntax:

```javascript
const greet = (name) => {
  return `Hello, ${name}!`;
};

// Even shorter for single expressions
const greet = name => `Hello, ${name}!`;

// Multiple parameters need parentheses
const add = (a, b) => a + b;

// No parameters need empty parentheses
const sayHello = () => "Hello!";
```

### Parameters and Arguments

```javascript
function introduce(name, age = 25) {  // age has a default value
  return `I'm ${name}, ${age} years old.`;
}

introduce("Jerome", 30);  // "I'm Jerome, 30 years old."
introduce("Sarah");       // "I'm Sarah, 25 years old."
```

### Return Values

Functions return `undefined` by default. Use `return` to send a value back:

```javascript
function square(n) {
  return n * n;
}

let result = square(4);  // 16
```

---

## Arrays

Arrays store ordered lists of values.

### Creating Arrays

```javascript
let fruits = ["apple", "banana", "cherry"];
let numbers = [1, 2, 3, 4, 5];
let mixed = [1, "two", true, null];
let empty = [];
```

### Accessing Elements

```javascript
let fruits = ["apple", "banana", "cherry"];
let numbers = [1, 2, 3, 4, 5];

fruits[0]        // "apple" (first element)
fruits[1]        // "banana"
fruits[2]        // "cherry"
fruits.length    // 3
fruits[fruits.length - 1]  // "cherry" (last element)

numbers[2];      // Access the third element (3)
numbers.length;  // 5
```

### Modifying Arrays

```javascript
let fruits = ["apple", "banana"];

fruits.push("cherry");     // Add to end → ["apple", "banana", "cherry"]
fruits.pop();              // Remove from end → ["apple", "banana"]
fruits.unshift("mango");   // Add to start → ["mango", "apple", "banana"]
fruits.shift();            // Remove from start → ["apple", "banana"]

fruits[1] = "grape";       // Replace element → ["apple", "grape"]
```

### Array Methods

```javascript
let numbers = [1, 2, 3, 4, 5];

// find — first element matching condition
numbers.find(n => n > 3);         // 4

// findIndex — index of first match
numbers.findIndex(n => n > 3);    // 3

// includes — check if exists
numbers.includes(3);              // true

// indexOf — position of element
numbers.indexOf(3);               // 2

// join — combine into string
numbers.join("-");                // "1-2-3-4-5"
numbers.join(", ");               // "5, 4, 3, 2, 1"

// slice — copy portion (doesn't modify original)
numbers.slice(1, 4);              // [2, 3, 4]

// splice — remove/insert elements (modifies original)
numbers.splice(2, 1);             // Removes 1 element at index 2

// concat — combine arrays
[1, 2].concat([3, 4]);            // [1, 2, 3, 4]

// reverse — reverse order (modifies original)
numbers.reverse();                // [5, 4, 3, 2, 1]

// sort — sort elements (modifies original)
numbers.sort((a, b) => a - b);    // Ascending
numbers.sort((a, b) => b - a);    // Descending
```

---

## Array Iteration Methods

These are essential. Master them.

### forEach

Execute a function for each element:

```javascript
let fruits = ["apple", "banana", "cherry"];

fruits.forEach(fruit => {
  console.log(fruit);
});
// apple
// banana
// cherry
```

### map

Transform each element, return new array:

```javascript
let numbers = [1, 2, 3, 4, 5];

let doubled = numbers.map(n => n * 2);
// [2, 4, 6, 8, 10]

let names = ["jerome", "sarah", "mike"];
let capitalized = names.map(name => name.toUpperCase());
// ["JEROME", "SARAH", "MIKE"]
```

### filter

Keep elements that pass a test:

```javascript
let numbers = [1, 2, 3, 4, 5, 6];

let evens = numbers.filter(n => n % 2 === 0);
// [2, 4, 6]

let people = [
  { name: "Jerome", age: 30 },
  { name: "Sarah", age: 17 },
  { name: "Mike", age: 25 }
];

let adults = people.filter(person => person.age >= 18);
// [{ name: "Jerome", age: 30 }, { name: "Mike", age: 25 }]
```

### reduce

Combine all elements into one value:

```javascript
let numbers = [1, 2, 3, 4, 5];

let sum = numbers.reduce((total, n) => total + n, 0);
// 15

// Breakdown:
// (0, 1) => 1
// (1, 2) => 3
// (3, 3) => 6
// (6, 4) => 10
// (10, 5) => 15
```

### Chaining Methods

```javascript
let products = [
  { name: "Laptop", price: 1000, inStock: true },
  { name: "Phone", price: 500, inStock: false },
  { name: "Tablet", price: 300, inStock: true }
];

let result = products
  .filter(p => p.inStock)
  .map(p => p.name)
  .join(", ");

// "Laptop, Tablet"
```

---

## Objects

Objects store key-value pairs.

### Creating Objects

```javascript
let person = {
  name: "Jerome",
  age: 30,
  isVeteran: true,
  skills: ["JavaScript", "HTML", "CSS"]
};

// Create the object
const person = {
  name: "Jody",
  age: 30,
  gender: "male",
  sayHello: function () {
    console.log("Hello!");
  },
};
```

### Accessing Properties

```javascript
// Dot notation
person.name          // "Jerome"
person.age           // 30

// Bracket notation (required for dynamic keys)
person["name"]       // "Jerome"

let key = "age";
person[key]          // 30

// Accessing the object
console.log(person.name); // Output: Jody
console.log(person["age"]); // Output: 30

person.sayHello(); // Output: Hello!
```

### Modifying Objects

```javascript
// Add/update properties
person.email = "jerome@example.com";
person.age = 31;

// Delete properties
delete person.email;

// Adding to or updating the object
person.age = 35;
person.job = "developer";

console.log(person.age); // Output: 35
console.log(person.job); // Output: developer

// Removing properties
delete person.gender;

console.log(person.gender); // Output: undefined
```

### Object Methods

```javascript
let person = { name: "Jerome", age: 30 };

Object.keys(person)      // ["name", "age"]
Object.values(person)    // ["Jerome", 30]
Object.entries(person)   // [["name", "Jerome"], ["age", 30]]
```

### Methods in Objects

Objects can contain functions:

```javascript
let calculator = {
  add: function(a, b) {
    return a + b;
  },
  subtract(a, b) {  // Shorthand
    return a - b;
  }
};

calculator.add(5, 3);      // 8
calculator.subtract(10, 4); // 6
```

### Destructuring

Extract values into variables:

```javascript
let person = { name: "Jerome", age: 30, city: "Atlanta" };

// Old way
let name = person.name;
let age = person.age;

// Destructuring
let { name, age } = person;

// With different variable names
let { name: personName, age: personAge } = person;

// Array destructuring
let [first, second] = ["a", "b", "c"];
// first = "a", second = "b"
```

### Spread Operator

```javascript
// Copy an object
let copy = { ...person };

// Merge objects
let merged = { ...person, email: "jerome@example.com" };

// Copy an array
let numbersCopy = [...numbers];

// Merge arrays
let combined = [...arr1, ...arr2];
```

---

## DOM Manipulation

The DOM (Document Object Model) is how JavaScript interacts with HTML.

### Selecting Elements

```javascript
// By ID
let header = document.getElementById("header");

// By class (returns collection)
let cards = document.getElementsByClassName("card");

// By tag (returns collection)
let paragraphs = document.getElementsByTagName("p");

// Modern way — CSS selectors (use these)
let header = document.querySelector("#header");       // First match
let cards = document.querySelectorAll(".card");       // All matches
let firstCard = document.querySelector(".card");      // First .card
let navLinks = document.querySelectorAll("nav a");    // All links in nav
```

### Modifying Content

```javascript
let element = document.querySelector("#title");

// Text content
element.textContent = "New Title";

// HTML content
element.innerHTML = "<strong>Bold Title</strong>";

// Form values
let input = document.querySelector("#email");
input.value = "test@example.com";
let currentValue = input.value;

document.getElementById("message").innerHTML = "Hello, World!";
```

### Modifying Attributes

```javascript
let link = document.querySelector("a");

// Get attribute
link.getAttribute("href");

// Set attribute
link.setAttribute("href", "https://example.com");

// Remove attribute
link.removeAttribute("target");

// Check if has attribute
link.hasAttribute("target");

// Direct property access (for common attributes)
link.href = "https://example.com";
link.id = "main-link";
```

### Modifying Classes

```javascript
let element = document.querySelector(".card");

// Add class
element.classList.add("active");

// Remove class
element.classList.remove("active");

// Toggle class (add if missing, remove if present)
element.classList.toggle("active");

// Check if has class
element.classList.contains("active");  // true or false

// Replace class
element.classList.replace("old-class", "new-class");
```

### Modifying Styles

```javascript
let element = document.querySelector(".box");

// Direct style (camelCase)
element.style.backgroundColor = "blue";
element.style.fontSize = "20px";
element.style.display = "none";

// Get computed style
let styles = getComputedStyle(element);
styles.backgroundColor;  // "rgb(0, 0, 255)"
```

---

## Events

Events respond to user actions.

### Adding Event Listeners

```javascript
let button = document.querySelector("#submit-btn");

button.addEventListener("click", function() {
  console.log("Button clicked!");
});

// Arrow function version
button.addEventListener("click", () => {
  console.log("Button clicked!");
});

// Named function (better for removal)
function handleClick() {
  console.log("Button clicked!");
}
button.addEventListener("click", handleClick);
```

### Common Events

| Event | Triggered when |
|-------|---------------|
| `click` | Element is clicked |
| `dblclick` | Element is double-clicked |
| `mouseenter` | Mouse enters element |
| `mouseleave` | Mouse leaves element |
| `keydown` | Key is pressed |
| `keyup` | Key is released |
| `submit` | Form is submitted |
| `change` | Input value changes (after blur) |
| `input` | Input value changes (immediately) |
| `focus` | Element gains focus |
| `blur` | Element loses focus |
| `scroll` | Page is scrolled |
| `load` | Page/image finishes loading |

### The Event Object

```javascript
button.addEventListener("click", function(event) {
  console.log(event.type);           // "click"
  console.log(event.target);         // The clicked element
  console.log(event.currentTarget);  // The element with the listener
});

// Form submission
form.addEventListener("submit", function(event) {
  event.preventDefault();  // Stop form from submitting
  // Handle form data with JavaScript instead
});

// Keyboard events
document.addEventListener("keydown", function(event) {
  console.log(event.key);    // "Enter", "a", "Escape"
  console.log(event.code);   // "Enter", "KeyA", "Escape"
});
```

### Event Delegation

Instead of adding listeners to many elements, add one to a parent:

```javascript
// Instead of this (bad for many items):
document.querySelectorAll(".card").forEach(card => {
  card.addEventListener("click", handleCardClick);
});

// Do this (one listener on parent):
document.querySelector(".card-container").addEventListener("click", function(event) {
  if (event.target.classList.contains("card")) {
    handleCardClick(event);
  }
});
```

---

## Creating and Removing Elements

### Creating Elements

```javascript
// Create element
let div = document.createElement("div");

// Add content and attributes
div.textContent = "Hello!";
div.classList.add("card");
div.id = "new-card";

// Add to the page
document.body.appendChild(div);

// Or insert at specific location
let container = document.querySelector(".container");
container.appendChild(div);

// Insert before another element
container.insertBefore(div, container.firstChild);
```

### Building Complex Elements

```javascript
function createCard(title, description) {
  let card = document.createElement("div");
  card.classList.add("card");

  card.innerHTML = `
    <h3>${title}</h3>
    <p>${description}</p>
    <button class="delete-btn">Delete</button>
  `;

  return card;
}

let newCard = createCard("My Card", "This is a description");
document.querySelector(".container").appendChild(newCard);
```

### Removing Elements

```javascript
let element = document.querySelector(".old-card");

// Modern way
element.remove();

// Old way (still works)
element.parentNode.removeChild(element);
```

---

## Local Storage

Store data in the browser that persists after page refresh.

### Basic Operations

```javascript
// Save data
localStorage.setItem("username", "Jerome");

// Get data
let username = localStorage.getItem("username");  // "Jerome"

// Remove data
localStorage.removeItem("username");

// Clear all data
localStorage.clear();
```

### Storing Objects and Arrays

localStorage only stores strings. Convert with JSON:

```javascript
// Save object
let user = { name: "Jerome", age: 30 };
localStorage.setItem("user", JSON.stringify(user));

// Get object
let stored = localStorage.getItem("user");
let user = JSON.parse(stored);

// Save array
let tasks = ["Learn JS", "Build portfolio", "Apply for jobs"];
localStorage.setItem("tasks", JSON.stringify(tasks));

// Get array
let tasks = JSON.parse(localStorage.getItem("tasks"));
```

### Practical Pattern

```javascript
// Save function
function saveToStorage(key, data) {
  localStorage.setItem(key, JSON.stringify(data));
}

// Load function with default
function loadFromStorage(key, defaultValue = null) {
  let data = localStorage.getItem(key);
  return data ? JSON.parse(data) : defaultValue;
}

// Usage
saveToStorage("settings", { theme: "dark", fontSize: 16 });
let settings = loadFromStorage("settings", { theme: "light", fontSize: 14 });
```

---

## Putting It Together

Here's how these concepts work together:

```javascript
// Data
let projects = [
  { id: 1, name: "Portfolio", category: "web", completed: true },
  { id: 2, name: "Calculator", category: "app", completed: false },
  { id: 3, name: "Blog", category: "web", completed: true }
];

// Render function
function renderProjects(projectList) {
  let container = document.querySelector("#projects");
  container.innerHTML = "";

  projectList.forEach(project => {
    let card = document.createElement("div");
    card.classList.add("project-card");
    if (project.completed) card.classList.add("completed");

    card.innerHTML = `
      <h3>${project.name}</h3>
      <span class="category">${project.category}</span>
      <button data-id="${project.id}">Toggle Complete</button>
    `;

    container.appendChild(card);
  });
}

// Filter function
function filterByCategory(category) {
  if (category === "all") {
    renderProjects(projects);
  } else {
    let filtered = projects.filter(p => p.category === category);
    renderProjects(filtered);
  }
}

// Event listeners
document.querySelector("#filter").addEventListener("change", function(event) {
  filterByCategory(event.target.value);
});

document.querySelector("#projects").addEventListener("click", function(event) {
  if (event.target.tagName === "BUTTON") {
    let id = parseInt(event.target.dataset.id);
    let project = projects.find(p => p.id === id);
    project.completed = !project.completed;
    renderProjects(projects);
  }
});

// Initial render
renderProjects(projects);
```

---

## Coding Challenges

Complete at least **30 challenges**. Write each from scratch.

### String Challenges

1. **Reverse a string** — `reverse("hello")` → `"olleh"`

2. **Check if palindrome** — `isPalindrome("racecar")` → `true`

3. **Count vowels** — `countVowels("hello")` → `2`

4. **Capitalize words** — `capitalize("hello world")` → `"Hello World"`

5. **Remove duplicates** — `removeDuplicates("hello")` → `"helo"`

### Array Challenges

6. **Find largest** — `findMax([1, 5, 3])` → `5`

7. **Sum all** — `sum([1, 2, 3])` → `6`

8. **Remove duplicates** — `unique([1, 2, 2, 3])` → `[1, 2, 3]`

9. **Flatten array** — `flatten([[1, 2], [3, 4]])` → `[1, 2, 3, 4]`

10. **Sort by property** — Sort array of objects by a given key

### Logic Challenges

11. **FizzBuzz** — Print 1-100, "Fizz" for 3s, "Buzz" for 5s, "FizzBuzz" for both

12. **Is prime** — `isPrime(7)` → `true`

13. **Factorial** — `factorial(5)` → `120`

14. **Fibonacci** — `fibonacci(7)` → `[0, 1, 1, 2, 3, 5, 8]`

15. **GCD** — `gcd(12, 8)` → `4`

### Object Challenges

16. **Merge objects** — Combine two objects

17. **Deep clone** — Copy object without reference

18. **Check equality** — Compare two objects deeply

19. **Array to object** — `toObject([["a", 1], ["b", 2]])` → `{a: 1, b: 2}`

20. **Group by property** — Group array items by a key

### Additional Challenges (10 more from Codewars)

Complete 10 challenges on [Codewars](https://www.codewars.com/) at 8 kyu or 7 kyu level.

Focus on:
- String manipulation
- Array operations
- Basic algorithms
- Object handling

---

## How to Know You're Ready

You should be able to do all of the following without looking anything up:

- [ ] Declare variables with let and const
- [ ] Use all data types appropriately
- [ ] Write conditional logic (if/else, switch, ternary)
- [ ] Write loops (for, while, for...of)
- [ ] Create and call functions
- [ ] Work with arrays and all common methods
- [ ] Work with objects
- [ ] Select and modify DOM elements
- [ ] Handle events
- [ ] Create and remove elements dynamically
- [ ] Use localStorage

---

## Your Gate

Keep a JavaScript file with all **30+ challenge solutions**.

You'll reference these when building your portfolio features and during your interview.

---

**Enjoy exploring the endless possibilities of web interactivity. 🚀**

---

**Next up:** [Module 6: Capstone — Your Portfolio](capstone.md)
