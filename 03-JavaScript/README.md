# ⚡ JavaScript Fundamentals - Panduan Lengkap

**JavaScript** adalah bahasa pemrograman untuk membuat halaman web interaktif dan dinamis. Pelajari variables, functions, DOM manipulation, dan async programming.

---

## 📋 Daftar Isi

1. [Variables & Data Types](#variables--data-types)
2. [Operators & Control Flow](#operators--control-flow)
3. [Functions](#functions)
4. [DOM Manipulation](#dom-manipulation)
5. [Events](#events)
6. [Async Programming](#async-programming)
7. [ES6+ Features](#es6-features)
8. [Best Practices](#best-practices)

---

## Variables & Data Types

### Deklarasi Variables:

```javascript
// var (old, hindari!) ❌
var name = "John";

// let (block scope) ✅
let age = 25;
let address;

// const (constant) ✅
const PI = 3.14159;
const person = { name: "Alice", age: 30 };
```

### Data Types:

```javascript
// String
const name = "John";
const greeting = `Hello, ${name}!`; // Template literal

// Number
const age = 25;
const price = 19.99;

// Boolean
const isActive = true;
const isEmpty = false;

// Array
const fruits = ["apple", "banana", "orange"];
const numbers = [1, 2, 3, 4, 5];

// Object
const person = {
    name: "John",
    age: 25,
    city: "Jakarta"
};
```

---

## Operators & Control Flow

### Arithmetic Operators:

```javascript
const a = 10;
const b = 3;

console.log(a + b);  // 13
console.log(a - b);  // 7
console.log(a * b);  // 30
console.log(a / b);  // 3.33...
console.log(a % b);  // 1 (remainder)
```

### Comparison Operators:

```javascript
console.log(5 === "5");  // false (strict equality) - GUNAKAN INI!
console.log(5 !== "5");  // true
console.log(5 > 3);      // true
console.log(5 < 3);      // false
```

### Conditional Statements:

```javascript
// if...else
if (age >= 18) {
    console.log("Dewasa");
} else if (age >= 13) {
    console.log("Remaja");
} else {
    console.log("Anak-anak");
}

// Ternary operator
const status = age >= 18 ? "Dewasa" : "Anak-anak";
```

### Loops:

```javascript
// for loop
for (let i = 0; i < 5; i++) {
    console.log(i);
}

// for...of (untuk array)
const fruits = ["apple", "banana", "orange"];
for (const fruit of fruits) {
    console.log(fruit);
}

// forEach
fruits.forEach((fruit, index) => {
    console.log(index, fruit);
});
```

---

## Functions

### Function Declarations:

```javascript
// Function declaration
function greet(name) {
    return `Hello, ${name}!`;
}
console.log(greet("John")); // "Hello, John!"

// Arrow function (ES6)
const multiply = (a, b) => a * b;
console.log(multiply(5, 3)); // 15
```

---

## DOM Manipulation

### Selecting Elements:

```javascript
// Get single element
const header = document.getElementById("header");
const mainContent = document.querySelector(".main-content");

// Get multiple elements
const paragraphs = document.querySelectorAll("p");
```

### Modifying Content:

```javascript
const element = document.querySelector("h1");
element.textContent = "New Title"; // Set text
element.innerHTML = "<em>New Title</em>"; // Set HTML
```

### Modifying Classes:

```javascript
const button = document.querySelector(".button");

button.classList.add("active");
button.classList.remove("disabled");
button.classList.toggle("highlight");
```

---

## Events

### Event Listeners:

```javascript
const button = document.querySelector(".button");

button.addEventListener("click", function(event) {
    console.log("Button clicked!");
});

// Arrow function
button.addEventListener("click", (e) => {
    console.log("Clicked!");
});
```

### Common Events:

```javascript
const input = document.querySelector("input");

// Input event (real-time)
input.addEventListener("input", (e) => {
    console.log("Value:", e.target.value);
});

// Submit event
const form = document.querySelector("form");
form.addEventListener("submit", (e) => {
    e.preventDefault(); // Prevent default
    console.log("Form submitted!");
});
```

---

## Async Programming

### Promises:

```javascript
const promise = new Promise((resolve, reject) => {
    setTimeout(() => {
        const success = true;
        if (success) {
            resolve({ id: 1, name: "John" });
        } else {
            reject("Error occurred");
        }
    }, 1000);
});

promise
    .then((data) => console.log("Success:", data))
    .catch((error) => console.log("Error:", error));
```

### Async/Await:

```javascript
async function getData() {
    try {
        const response = await fetch("/api/users");
        const data = await response.json();
        console.log("Data:", data);
    } catch (error) {
        console.log("Error:", error);
    }
}

getData();
```

### Fetch API:

```javascript
// GET request
fetch("/api/users")
    .then((response) => response.json())
    .then((data) => console.log(data))
    .catch((error) => console.log(error));
```

---

## Best Practices

### 1. Gunakan const by default
```javascript
// ✅ Benar
const PI = 3.14;
let count = 0;

// ❌ Hindari
var name = "John";
```

### 2. Gunakan Strict Equality
```javascript
// ✅ Benar
if (age === 18) { }

// ❌ Hindari
if (age == "18") { }
```

---

## 🔗 Resources

- [MDN JavaScript Documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
- [JavaScript Info](https://javascript.info/)

---

[← Kembali ke CSS](../02-CSS-Styling/README.md) | [← Main](../README.md) | [Lanjut ke Responsive Design →](../04-Responsive-Design/README.md)
