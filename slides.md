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

# Month 2 Week 3

Modularity in programming refers to breaking down a complex system into separate, self-contained units (modules) that each handle a specific function.

Imports and exports features are the mechanism that makes modularity possible in modern JavaScript. They create the connections between separate modules, allowing them to work together while remaining independent.

Example of Use of the Import/Export Feature

```javascript
export function createList(item) {

 const li = document.createElement ('li')
  li.textContent = item
  return li
}

import {createList} from source directory (./utils/createList.js)
```

<!--
This is a **note**
-->

---

# Features in a Todo App

1. Update Todo.

```javascript
export function editFunction(span) {
  const input = document.createElement("input");
  input.value = span.textContent;
  span.parentNode.replaceChild(input, span);
  input.focus();

  input.addEventListener("blur", function () {
    span.textContent = input.value.trim() || span.textContent;
    input.parentNode.replaceChild(span, input);
    saveTodos(getAllTodos());
  });
}
```

2. Delete Todo

```javascript
todoList.addEventListener('click', (e) => {
  // Delete todo
  if (e.target.classList.contains('delete-btn')) {
    e.target.parentNode.remove();
    saveTodos(getAllTodos());
  }
})
```
<!--Code Block for features for a todo App-->

---

# Vite what it is and how it works
Vite is a modern front-end build tool that includes bundling functionality. It's designed as a faster alternative to traditional bundlers like Webpack.

Vite operates differently from traditional bundlers and has two distinct modes

Development: 

-Uses native ES modules in browsers

-No bundling during development - serves individual files on demand

-Lightning-fast Hot Module Replacement (HMR)

-Optimizes dependencies separately (pre-bundles them with esbuild)

Production: 

-Uses Rollup for production builds

-Code-splitting, tree-shaking, and modification

-Generates optimized assets for production deployment

---

How to Initialize Vite:

The Long Process 
````
create directory -  mkdr new-project
enter project directory- cd new-project
create package json-  npm init -y
install the bundler vite as a dev dependencies- npm i --save dev vite
install project files- touch.index{html,CSS,js}
set up git ignore- g ignore node >> .gitignore
set up scripts in the package.json file(dev: Vite, Build: Vite Build & Preview: Vite Preview)
start the project npm run dev

````
The Short Process
````
Initialize Vite- npm create vite @latest new-project
select framework
Enter project directory - cd new-project
start project- npm install & npm run dev

`````

---
