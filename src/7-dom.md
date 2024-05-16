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

# Javascript DOM

Document Object Model

<!--
_class: lead
_paginate: skip
-->

---
## The HTML DOM 

When a web page is loaded, the browser creates a _Document Object Model_ of the page.

--- 

## The HTML DOM Tree of Objects

![bg right contain](./images/dom-1.gif)

```html
<html>
  <head>
    <title>
    </title>
  </head>
  <body>
    <h1>My Hedaer</h1>
    <a href="">My Link</a>
  </body>
</html>
```

---

## What is the HTML DOM

The HTML DOM is a standard `object` model and `programming interface`for HTML. It defines:

- The HTML elements as `objects`
- The `properties` of all HTML elements
- The `methods` to access all HTML elements
- The `events` for all HTML elements

---

## Example

```html
<html>
  <body>
    <p id="demo"></p>

    <script>
      document.getElementById("demo").innerHTML = "Hello World!";
    </script>
  </body>
</html>
```

---

## Finding HTML Elements

|Method	|Description|
|---|---|
|*document.getElementById(id)*|	Find an element by element id|
|*document.getElementsByTagName(name)*|	Find elements by tag name|
|*document.getElementsByClassName(name)*|	Find elements by class name|

---

## Changing HTML Elements

<style scoped>
  table {
    font-size: 0.9rem;
  }
</style>

|Property	|Description|
|---|---|
|*element.innerHTML =  new html content*|	Change the inner HTML of an element|
|*element.attribute = new value*|	Change the attribute value of an HTML element|
|*element.style.property = new style*|	Change the style of an HTML element|

|Method	|Description|
|---|---|
|*element.setAttribute(attribute, value)*|	Change the attribute value of an HTML element|

---

## Adding and Deleting Elements

|Method|	Description|
|---|---|
|*document.createElement(element)*	|Create an HTML element|
|*document.removeChild(element)*	|Remove an HTML element|
|*document.appendChild(element)*	|Add an HTML element|
|*document.replaceChild(new, old)*	|Replace an HTML element|
|*document.write(text)*|	Write into the HTML output stream|

---

## Adding Events Handlers

|Method|	Description|
|---|---|
|*document.getElementById(id).onclick = function(){code}*|	Adding event handler code to an onclick event|

---

## Assignments

1. Buatlah permainan tebak angka sederhana menggunakan HTML dan JavaScript. Komputer akan memilih angka acak antara 1 dan 100. Pengguna diminta memasukkan tebakan, dan program akan memberi tahu apakah tebakannya terlalu besar, terlalu kecil, atau benar. 
2. Buatlah sebuah aplikasi todo list sederhana. Pengguna dapat menambahkan tugas baru, menandai tugas yang sudah selesai, dan menghapus tugas yang tidak diperlukan. Gunakan JavaScript untuk memanipulasi daftar tugas dalam DOM.