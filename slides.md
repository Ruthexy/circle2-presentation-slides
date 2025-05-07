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

<!--
- Month 1 Week 3
-->

---

# Summary Of LMS Month 1 week 3.

# Application Programming Interface(API)

Responsibilities of a frontend engineer
There are two basic responsiblities :

- Building of UI(User Interface) which is the primary
  responsibility
- Ensuring the UI is functioning.

# API

What is an API?

API means Application Programming Interface. It is like a messenger that lets two systems talk to each
other. It provides a way to sign up and sign in.

# Example:

Practical example to help understand how API work:

When the frontend form submits data to a server
(like logging in), it uses an API to send that data to the
backend. The API then responds back with the result.

<!--
- Month 1 Week 3 cont
-->

---

# Types of API requests:

There are several types of API requests, some are:

POST, GET, PATCH, DELETE......

# GET Request (Fetch or Retrieve Data)

What it does:

A GET request is used to retrieve data from a server. It
is a single way to fetch Information from a particular
data base.

# Real life example:

Real life example of a get request:

sending a get request to the backend to fetch for user
Email, full name...from a form. also,
you can fetch the user id from the database.

<!--
- Month 1 Week 3 cont
-->

---

# Code example - GET

Let’s say you open a weather app. The app sends a GET request to the API:

you send this:

```
GET https://weatherapi.com/today?city=Lagos
```

The server responds with:

```json
{
  "city": "Lagos",
  "temperature": "31°C",
  "condition": "Sunny"
}
```

# GET Request Status codes:

Here are some status codes to note:

- 200 - OK
- 201 - Created
<!--
- Month 1 Week 3 cont
  -->

---

- 302 - Redirect
- 404 - Not found
- 403 - Forbidden
- 405 - Method not allowed
- 401 - Unauthorized
- 500 - Server Error

# POST Request (Send or Submit Data)

What it does:

A POST request is used to send data to the server, like
submitting a form. POST is to send out info.

# Real-life example

Below is an example of POST request:

You’re signing up on a site.

<!--
- Month 1 Week 3 cont
  -->

---

# Code example - POST

Let examine the code below:

The form sends a POST request:

```
POST https://api.example.com/signup
```

with this body:

```json
{
  "name": "Pelumi",
  "email": "pelumi@example.com",
  "password": "12345"
}
```

The server responds:

```json
{
  "message": "Signup successful",
  "userId": 107
}
```

<!--
- Month 1 Week 3 conclusion
  -->

---

# 🧩 Summary

- APIs connect frontend to backend
- Use GET to **fetch**, POST to **send**
- Always watch status codes 🔍

<!-- https://sli.dev/guide/animations.html#click-animation -->

---

## transition: fade-out

# Month 1 - Week 1

This week started of with an advice to take the 'Learning how to learn course on coursera. <br>
_Books like:_ Refactoring UI, Frontend Developer Handbook and Simplified JavaScript for very important Programmers were listed as materials to help the learning process.

We were re-informed about array methods. Most notably the array.length.

Then:

```ts {monaco-run}
let name = "setemi";
console.log(name.length);
// The .length method returns the length of an array.
for (let each of name) {
  console.log(each);
}
```

---

## transition: slide-left

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
let obj = { name: "ojo", age: 12 };
let copied = { ...obj };
console.log(copied);
```

```ts {monaco-run}
//It is possible to spread and change the name:
let obj = { name: "ojo", age: 12 };
let copied = { ...obj, name: "Ola" };
console.log(copied);
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
}
example(1, 2, 3, 4, 5);
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

---

