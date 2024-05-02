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

- JavaScript and Java are completely different languages, both in concept and design.
- JavaScript was invented by Brendan Eich in 1995, and became an ECMA standard in 1997.
- ECMA-262 is the official name of the standard. ECMAScript is the official name of the language.

---

# Javascript Version

- The Original JavaScript ES1 ES2 ES3 (1997-1999)
- The First Main Revision ES5 (2009)
- The Second Revision ES6 (2015)
- The Yearly Additions (2016, 2017 ... 2021, 2022)

---

# JavaScript Where To

- The `<script>` Tag

---

# The `<script>` Tag

In HTML, JavaScript code is inserted between `<script>` and `</script>` tags.

```html
<script>
document.getElementById("demo").innerHTML = "My First JavaScript";
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
    function myFunction() {
      document.getElementById("demo").innerHTML = "Paragraph changed.";
    }
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
    function myFunction() {
      document.getElementById("demo").innerHTML = "Paragraph changed.";
    }
  </script>
</body>
</html>
```
---

# External JavaScript

```js
// myScript.js
function myFunction() {
  document.getElementById("demo").innerHTML = "Paragraph changed.";
}
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

---

# JavaScript Output

JavaScript can "display" data in different ways:

- Writing into an HTML element, using `innerHTML`.
- Writing into the HTML output using `document.write()`.
- Writing into an alert box, using `window.alert()`.
- Writing into the browser console, `using console.log()`.

---

