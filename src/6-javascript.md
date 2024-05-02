---
marp: true
theme: gaia
paginate: true
footer: https://github.com/ibbi-ti-ii-p1/slide-ibbi-pemograman-web
style: |
  section::after {
    content: 'Page ' attr(data-marpit-pagination) ' / ' attr(data-marpit-pagination-total);
  }
---

# Javascript

The programming language of the Web.

<!--
_class: lead
_paginate: skip
-->

---
# What is Javascript

- JavaScript is a programming language used to make web pages more interactive and dynamic. 
- Javascript runs on the client-side (browser) and can be integrated with HTML and CSS to provide additional functionality to web pages. 
- JavaScript was initially developed by Brendan Eich of Netscape in 1995 and is now standardized by ECMA International.

---

# Version

- The Original JavaScript ES1 ES2 ES3 (1997-1999)
- The First Main Revision ES5 (2009)
- The Second Revision ES6 (2015)
- The Yearly Additions (2016, 2017 ... 2021, 2022)

---

# Where To

- Inline Javascript
- Internal Javascript
- External Javascript

---

# Inline Javascript


```html
<button onclick="alert('Hello, world!')">Click me</button>
```
---

# Common HTML Events

| Event       | Description                                        |
| ----------- | -------------------------------------------------- |
| onchange    | An HTML element has been changed                   |
| onclick     | The user clicks an HTML element                    |
| onmouseover | The user moves the mouse over an HTML element      |
| onmouseout  | The user moves the mouse away from an HTML element |
| onkeydown   | The user pushes a keyboard key                     |
| onload      | The browser has finished loading the page          |

---

# Internal Javascript

In HTML, JavaScript code is inserted between `<script>` and `</script>` tags.

```html
<button>Click me</button>
<script>
  document.querySelector('button').addEventListener('click', () => {
      alert('Hello, world!');
  });
</script>
```

---

# JavaScript in `<head>` or `<body>`

You can place any number of scripts in an HTML document.

Scripts can be placed in the `<body>`, or in the `<head>` section of an HTML page, or in both.

---

# JavaScript in `<head>`

```html
<!DOCTYPE html>
<html>
<head>
  <script>
    document.querySelector('button').addEventListener('click', () => {
        alert('Hello, world!');
    });
</script>
</head>
<body>
  ...
</body>
</html>
```
---

# JavaScript in `<body>`

```html
<!DOCTYPE html>
<html>
<body>
  ...
  <script>
    document.querySelector('button').addEventListener('click', () => {
        alert('Hello, world!');
    });
</script>
</body>
</html>
```
---

# External JavaScript

```js
// myScript.js
<script>
  document.querySelector('button').addEventListener('click', () => {
      alert('Hello, world!');
  });
</script>
```

```html
<!-- index.html -->
<script src="myScript.js"></script>
```

---

# External JavaScript Advantages

- It separates HTML and code
- It makes HTML and JavaScript easier to read and maintain
- Cached JavaScript files can speed up page loads
- It can be reused
---

# JavaScript Output

JavaScript can "display" data in different ways:

- Writing into an HTML element, using `innerHTML`.
- Writing into the HTML output using `document.write()`.
- Writing into an alert box, using `window.alert()`.
- Writing into the browser console, using `console.log()`.

---

# Variables

Variables are Containers for Storing Data, javaScript variables can be declared in 4 ways:

- Using `var`
- Using `let`
- Using `const`
  

---

# When to Use var, let, or const?

- Always declare variables
- Always use `const` if the value should not be changed
- Only use `let` if you can't use `const`
- Only use `var` if you MUST support old browsers.

---

# Variable Syntax

```js
const price1 = 5;
const price2 = 6;
let total = price1 + price2;
```

---

# Variable Identifiers

- All JavaScript variables must be identified with unique names.
  
- These unique names are called identifiers.
  
- Identifiers can be short names (like x and y) or more descriptive names (age, sum, totalVolume).


---

# The Variable Identifier Rules

The general rules for constructing names for variables are:

- Names can contain letters, digits, underscores, and dollar signs.
- Names must begin with a letter.
- Names can also begin with $ and _ (but we will not use it in this tutorial).
- Names are case sensitive (y and Y are different variables).
- Reserved words (like JavaScript keywords) cannot be used as names.

---

# Operators

<style scoped>
  table {
    font-size: 0.8rem;
  }
</style>

| Operator | Description                  |
| -------- | ---------------------------- |
| +        | Addition                     |
| -        | Subtraction                  |
| *        | Multiplication               |
| **       | Exponentiation (ES2016)      |
| /        | Division                     |
| %        | Modulus (Division Remainder) |
| ++       | Increment                    |
| --       | Decrement                    |

---

# Assignment Operators

<style scoped>
  table {
    font-size: 0.9rem;
  }
</style>

| Operator | Example | Same As    |
| -------- | ------- | ---------- |
| =        | x = y   | x = y      |
| +=       | x += y  | x = x + y  |
| -=       | x -= y  | x = x - y  |
| *=       | x *= y  | x = x * y  |
| /=       | x /= y  | x = x / y  |
| %=       | x %= y  | x = x % y  |
| **=      | x **= y | x = x ** y |

---

# Comparison Operator

<style scoped>
  table {
    font-size: 0.75rem;
  }
</style>

| Operator | Description                       |
| -------- | --------------------------------- |
| ==       | equal to                          |
| ===      | equal value and equal type        |
| !=       | not equal                         |
| !==      | not equal value or not equal type |
| >        | greater than                      |
| <        | less than                         |
| >=       | greater than or equal to          |
| <=       | less than or equal to             |
| ?        | ternary operator                  |

---

# Logical Operator

| Operator | Description |
| -------- | ----------- |
| &&       | logical and |
| \|\|     | logical or  |
| !        | logical not |

---

# Data Types

<style scoped>
  li {
    font-size: 0.85rem;
  }
</style>

JavaScript has 8 Datatypes
1. String
2. Number
3. Bigint
4. Boolean
5. Undefined
6. Null
7. Symbol
8. Object
  
----
# Data Types Examples

```js
// Numbers:
let length = 16;
let weight = 7.5;

// Strings:
let color = "Yellow";
let lastName = "Johnson";

// Booleans
let x = true;
let y = false;


```

---
# The Object Data Types

The object data type can contain:

1. An object
2. An array
3. A date

---

# The Object Data Types Examples


```js
// Object:
const person = {firstName:"John", lastName:"Doe"};

// Array object:
const cars = ["Saab", "Volvo", "BMW"];

// Date object:
const date = new Date("2022-03-25");
```

---

# Functions

- A JavaScript function is a block of code designed to perform a particular task.

- A JavaScript function is executed when "something" invokes it (calls it).

---

# Function Syntax

```js
function name(parameter1, parameter2, parameter3) {
  // code to be executed
}
```

---

# Function Example

```js
// Function to compute the product of p1 and p2
function myFunction(p1, p2) {
  return p1 * p2;
}
```

---

# Function Return

Functions often compute a return value. The return value is "returned" back to the "caller":

```js
// Function is called, the return value will end up in x
let x = myFunction(4, 3);

function myFunction(a, b) {
// Function returns the product of a and b
  return a * b;
}
```

--- 

# Why Functions?

- With functions you can reuse code

- You can write code that can be used many times.

- You can use the same code with different arguments, to produce different results.

--- 

# if, else, and else if

In JavaScript we have the following conditional statements:
- Use `if` to specify a block of code to be executed, if a specified condition is true
- Use `else` to specify a block of code to be executed, if the same condition is false
- Use `else if` to specify a new condition to test, if the first condition is false
- Use `switch` to specify many alternative blocks of code to be executed

---

# if, else and else if Example

```js
if (time < 10) {
  greeting = "Good morning";
} else if (time < 20) {
  greeting = "Good day";
} else {
  greeting = "Good evening";
}
```

---

# Switch Example

```js
switch (new Date().getDay()) {
  case 0:
    day = "Sunday";
    break;
  case 1:
    day = "Monday";
    break;
  case 2:
     day = "Tuesday";
    break;
  ...
}
```

---

# For Loop

Loops are handy, if you want to run the same code over and over again, each time with a different value.

```js
text += cars[0] + "<br>";
text += cars[1] + "<br>";
text += cars[2] + "<br>";
text += cars[3] + "<br>";
text += cars[4] + "<br>";
text += cars[5] + "<br>";
```

```js
for (let i = 0; i < cars.length; i++) {
  text += cars[i] + "<br>";
}
```

---

# Different Kinds of Loops

JavaScript supports different kinds of loops:

- `for` -  loops through a block of code a number of times
- `for/in` - loops through the properties of an object
- `for/of` - loops through the values of an iterable object
- `while` -  loops through a block of code while a specified condition is true
- `do/while` - also loops through a block of code while a specified condition is true

---

# For In

The JavaScript for in statement loops through the properties of an Object:

```js
const person = {fname:"John", lname:"Doe", age:25};

let text = "";
for (let x in person) {
  text += person[x];
}
```

---

# For Of

The JavaScript for of statement loops through the values of an iterable object.

```js
const cars = ["BMW", "Volvo", "Mini"];

let text = "";
for (let x of cars) {
  text += x;
}
```

---

# While Loop

Loops can execute a block of code as long as a specified condition is true.

```js
while (i < 10) {
  text += "The number is " + i;
  i++;
}
```

```js
do {
  text += "The number is " + i;
  i++;
}
while (i < 10);
```
---

# Assignments

- Buatlah sebuah program sederhana menggunakan JavaScript yang dapat menghitung luas dan keliling lingkaran berdasarkan input jari-jari dari pengguna.

- Buatlah sebuah program yang dapat menghitung nilai rata-rata dari serangkaian angka yang dimasukkan oleh pengguna. Program harus terus meminta pengguna untuk memasukkan angka hingga pengguna memasukkan nilai tertentu (misalnya 0) untuk menghentikan input.