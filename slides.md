---
# You can also start simply with 'default'
theme: seriph
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://cover.sli.dev
# some information about your slides (markdown enabled)
title: Welcome to Slidev
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

---
transition: fade-out
---

# Month 1 - Week 1

This week started of with an advice to take the 'Learning how to learn course on coursera. <br>
*Books like:* Refactoring UI, Frontend Developer Handbook and Simplified JavaScript for very important Programmers were listed as materials to help the learning process.

We were re-informed about array methods. Most notably the array.length.

Then:
```ts {monaco-run}
let name = 'setemi'
console.log(name.length);
// The .length method returns the length of an array. 
for (let each of name) {
     console.log(each);
}
```

---
transition: slide-left
---

# Spread Operators and Rest parameters.

**The spread operator (...) in JavaScript is used to "spread out" elements of an array (or object) into individual elements.**

<div grid="~ cols-2 gap-2" m="t-2">

```yaml
---
Say we have an array:
arr = ['a', 'b', 'c'];
console.log(arr)
// ['a', 'b', 'c']

let newArr = [...arr];
console.log(newArr)
// ['a', 'b', 'c']
---
```

```yaml
---
Combining two arrays:
Let copied = ['a', 'b', 'c']
console.log(copied)
// ['a', 'b', 'c']

Let newCopied = [...copied, 'd', 'e', 'f']
console.log(newCopied)
// ['a', 'b', 'c', 'd', 'e', 'f']
---
```


```ts {monaco-run}
//On an object:
let obj = {name: 'ojo', age: 12};
let copied = {...obj};
console.log(copied)
```

```ts {monaco-run}
//It is possible to spread and change the name:
let obj = {name: 'ojo', age: 12};
let copied = {...obj, name: 'Ola'};
console.log(copied)
```


</div>

---
transition: slide-down
class: px-20
---

# Rest

The rest parameter syntax in Javascript allows a function to accept any number of arguments as an array. This is useful when you don't know how many arguments will be passed in, or when you want to simplify handling multiple inputs.
```ts {monaco-run}
function example(first, second, ...others) {
   // logs first and second arguments
   //alert(first, second)
   // logs the rest of the arguments as an array
   //alert(others)
};
example(1,2,3,4,5)
```
# Callbacks
```ts
// Callback functions are functions that are called when certain parameters are met. 
function callbackEx (message, yesFn, noFn) {
     let result = confirm(message);
     if (result) yesFn()
     else noFn()
//If the if statement is just 1, no curly braces needed
} 
callbackEx('Do you have a boyfriend', () => console.log('yes'), () => console.log('no'
```
<<<<<<< m1-week2
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
=======
---
transition: fade-out
---
