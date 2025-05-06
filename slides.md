---
# You can also start simply with 'default'
theme: seriph
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://cover.sli.dev
# some information about your slides (markdown enabled)
title: 
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
# apply unocss classes to the current slide
class: text-center
# https://sli.dev/features/drawing
drawings:
  persist: false
# slide transition: https://sli.dev/guide/animations.html#slide-transitions
transition: slide-left
# enable MDC Syntax: https://sli.dev/features/mdc
mdc: true
# open graph
# seoMeta:
#  ogImage: https://cover.sli.dev
---

# Circle 2 Assignment Presentation Slides

<div @click="$slidev.nav.next" class="mt-12 py-1" hover:bg="white op-10">
  Press Space for next page <carbon:arrow-right />
</div>

<div class="abs-br m-6 text-xl">
  <button @click="$slidev.nav.openInEditor()" title="Open in Editor" class="slidev-icon-btn">
    <carbon:edit />
  </button>
  <a href="https://github.com/slidevjs/slidev" target="_blank" class="slidev-icon-btn">
    <carbon:logo-github />
  </a>
</div>

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

---

# Circle 2 Members

- Ayomide Ohiokhara Akhatevbeda
- Chiamaka Faith Nwokolo
- Alex Ekpendu
- Adegoke Anuoluwa
- Pelumi Ajiteru
- Ruth Okwuokenye
- Soliah Oluwapelumi Akinola
- Theophilus Chika Amadi
- Ogunleye Michael
- Kelechi Ejikeme
  <br>
  <br>

<!--
You can have `style` tag in markdown to override the style for the current page.
Learn more: https://sli.dev/features/slide-scope-style
-->

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

<!--
Here is another comment.
-->

---

# Table of Contents

- Month 1 Week 1
- Month 1 Week 2
- Month 1 Week 3
- Month 1 Week 4
- Month 2 Week 1
- Month 2 Week 2
- Month 2 Week 3
- Month 2 Week 4

<!-- https://sli.dev/guide/animations.html#click-animation -->

---

# Summary of Month 1 Week 2 – Second Semester Class

## Key Points
- Functions
- Callbacks
- Events
- Event Handlers
- Promises

---

# Functions

A **function** is a reusable block of code that performs a specific task. You can define it once and call it whenever needed.

```js
function greet(name) {
  console.log("Hello, " + name + "!");
}

greet("Ada"); // Output: Hello, Ada!
```

---

# Closures

A function that returns another function is called a **closure**.

```js
function add(val1) {
  return function (val2) {
    return val1 + val2;
  };
}

let addTwoFn = add(2);
console.log(addTwoFn(15)); // Output: 17
```

---

# Callbacks

Callbacks are used to execute a function **after** another function finishes. This is especially useful when dealing with asynchronous operations.

For example, 

```js
const getAverageResult = () => {
    let result = [2, 3, 4, 5, 6, 7, 8];
    // using callback function to calculate the average of an array of numbers
    const callback = (acc, num) => acc + num;
    let sum = result.reduce(callback, 0);
    console.log(sum)
    let average = sum / result.length;
    alert(average);
  }
  getAverageResult()
```

---

## Array Methods That Use Callbacks

- `.reduce()`
- `.filter()`
- `.map()`
- `.forEach()`
- `.every()`
- `.some()`
- `.find()`

---

## Example Using `.reduce()`
the **callback** of `.reduce()` can take and accept mazimum of four parameters or less.

code example using 2 parameters

```js
/*
Function to calculate the average of an array of numbers
using the reduce method to calculate the sum and divide
by the array's length.
*/

const getAverage = () => {
  let result = [2, 3, 4, 5, 6, 7, 8];
  let sum = result.reduce((acc, num) => acc + num, 0);
  let average = sum / result.length;
  
  alert(average); // Output: 5
};

getAverage();
```

---

# Events and Handlers

An **event** is an action that occurs in the browser (e.g., a button click). An **event handler** is a function that runs in response to an event.

# three ways to create event
- `addEventListener`
- `HTML attribute`
- `DOM`

code example

```js
document.getElementById("btn").addEventListener("click", function () {
  alert("Button was clicked!");
});
```

---

# Promises

A **promise** is an object that represents the eventual completion (or failure) of an asynchronous operation.

```js
const fetchData = new Promise((resolve, reject) => {
  let success = true;

  if (success) {
    resolve("Data fetched successfully");
  } else {
    reject("Failed to fetch data");
  }
});

fetchData
  .then((msg) => console.log(msg))
  .catch((err) => console.error(err));
```
it is stated that if you have a function and you put `async` infront of the function, it becomes a `promise` and you need to `await` that data
it is also stated that, you can promisify an existing callback

---

# introduced these in promises
- `new`
- `return`
- `.then()`
- `.catch()`
- `fetch`
- `.json`
- `await`
- `try`
- `immediatelyinvoked function Expression(IIFE)`

# fetch
it says that it is a built in mechanism to communicate to an internal resource

---

# Summary

- Functions can return other functions (closures)
- Callbacks allow for dynamic behavior
- Array methods like `.map()`, `.reduce()`, and `.filter()` use callbacks
- Events and handlers connect user actions to code
- Promises handle asynchronous tasks cleanly