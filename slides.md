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
  console.log(sum);
  let average = sum / result.length;
  alert(average);
};
getAverageResult();
```

---

## transition: fade-out

# API Basics - LMS Month 1 Week 3

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
- 302 - Redirect
- 404 - Not found
- 403 - Forbidden
- 405 - Method not allowed
- 401 - Unauthorized
- 500 - Server Error

---

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

# Summary of month 1 week 4

This week talked mostly about ECMASCRIPT,DOM and walking the DOM TREE

ECMASCRIPT is the specification that describes JS. It is the formular sheet of Javascript. The host environment is the browser that contains that specification. There is JavaScript the language and JavaScript in the browser. This language specification describes how JavaScript is supposed to function in a browser.

- DOM ( Document Object Method): In simple terms; DOM is like JavaScript is trying to understand our HTML and CSS and it will turn all the HTML into objects. The parent of the object is called DOCUMENT.
- CSSOM ( CSS Object Model): Is the interface between JavaScript and CSS. It allows JavaScript to interact with the CSS.
- BOM ( Browser Object Model): is the interface between JavaScript and the browser. It allows JavaScript to interact with the browser. window object is the main object of the BOM. It represents the browser window. It allows web scripting - allowing JavaScript to interact with the browser as a interface to the host computer.

---

# DOM Tree and Walking the DOM

DOM in a nutshell is a tree representation of HTML.

```ts {monaco run}
console.log(document.documentElement); console.log(document.body); console.log(document.head); console.log(document.title);

HTMLHtmlElement: {}
HTMLBodyElement: {}
HTMLHeadElement: {}
JavaScript Class Note - AltSchool Africa
```

The nodes are connected in a tree structure, parent-child relationship, sibling relationship, next-previous relationship, first-last relationship, ancestor-descendant relationship, root-leaf relationship, text-element relationship and in a document type.

---

# DOM,BOM AND CSSOM

````ts
const element = document.querySelector(`[data-slidev-no="188"]`); // query selector is used to search
const h1 = element.querySelector('h1'); // if there are a bunch of divs,the query selector here is told to locate only the h1 element
// any valid selector that you can write in your CSS is what you can pass in your document.queryselector
console.log(h1.textContent)

h1.classList.add('text-gradient');
setTimeout(() => h1.classList.remove('text-gradient'), 3000); // return back

---

# WALKING THE DOM

You can now traverse the DOM tree using the following based the relationships between the nodes:
- parentNode, childNodes, firstChild, lastChild, nextSibling, previousSibling
- parentElement, children, firstElementChild, lastElementChild, nextElementSibling, previousElementSibling
## Searching: getElement*, querySelector*
You can search for elements in the DOM tree using the following methods:
- getElementById, getElementsByClassName, getElementsByTagName, getElementsByName
- querySelector, querySelectorAll
- matches, closest.

---


# Month 2 Week 1

 Searching The DOM

An Element with the id 'app' can be assigned to the element variable in two ways;

``` ts
const element = document.querySelector('#app')

const element = document.getElementById('app')
````

We search the DOM using document.querySelector or document.getElementById .
The element.innerHTML property allows us to set the HTML content of an element.

## Changing the DOM

Here, we learnt how to add, remove and update elements in the DOM. We also learnt that Adding HTML Elements, Text, Comments, Attributes, Properties and styles are some of the ways to change the DOM.

---

# Importing CSS in Javascript

To do this,

```ts
import "./styles.css";
```

# Adding HTML using innerHTML Property

```ts
elements.innerHTML = `
   <div>
      Hello There!
    </div>
`;
```

# Adding Texts and Elements

After creating the element, we add it to the DOM using appendChild or insertBefore.
Other ways to add elements to the DOM is prepend, append, before and after method.

# Removing Elements from the DOM

This is done using the remove method

```
element.remove();
```

---

# Update Text

The textContent property allows us to set the text content of an element

# EVENTS

These are actions that happen in a browser that you can listen for and respond to. Like, when you press a key, when you load a page, when you submit a form, when you click a button. These are all events.

We listen for events and respond to them with Event Listeners.

To demonstrate how events works in js using a counter:

````ts
export function setUpCounter(element) {
  let counter=0;

  const setCounter = (count) => {
    counter = count;
    element.innerHTML = `count is ${counter}`;
  };

+    element.addEventListener('click', () => setCounter(counter +1));

    setCounter(0);
}


---
# Month 2 Week 2

In the Month two, Week two class, the tutor, Setemi asked about our understanding of the previous class content, which was about our understanding of DOM, working with DOM

Then, we went into the class proper, in which we built a Todo app from scratch.

What do we need for a Todo application?

- Input field,
- Delete button
- Add button
- A list of possible todo.

---

#The HTML code block of the Todo App

```html
<h2>Todo App</h2>
<form>
  <div class="form-input">
    <label for="todo"></label>
    <input
      type="text"
      id="todo"
      placeholder="enter todo"
      required
      minlength="2"
      maxlength="100"
    />
  </div>
  <button>create todo</button>
</form>

<section class="display-todos">
  <ol>
    <li>Dance</li>
    <li>Eat</li>
    <li>Code</li>
  </ol>
</section>
````

---

#The Todo App

  <h2>Todo App</h2>
  <form>
    <div class="form-input">
      <label for="todo"></label>
      <input 
        type="text" 
        id="todo" 
        placeholder="enter todo" 
        required 
        minlength="2" 
        maxlength="100"
      />
    </div>
    <button>create todo</button>
  </form>

  <section class="display-todos">
    <ol>
      <li>Dance</li>
      <li>Eat</li>
      <li>Code</li>
    </ol>
  </section>

---

#The CSS of our Todo App

```css
[data-name] {
  color: red;
}

.form-input {
}

button {
  margin-top: 8px;
}
```

---

JavaScript for the Todo App

```javascript
// named import
import { todoSubmitHandler } from "./src/submitHandler.js";
import { sayBye, person, sayHi } from "./src/say.js";
import { loadTodos } from "./src/submitHandler.js";
console.log("✅ index.js loaded");
// 📁 renamed import
import { sayHi as hi, sayBye as bye, person as angel } from "./src/say.js";
// import everything
import * as say from "./src/say.js";
// default import
// import sum from "./sum.js";

//
let todoForm = document.querySelector("#todoForm");
let todoList = document.querySelector("#todoList");

say.sayBye("Bolu");
say.sayHi("Jane");

hi("John"); // Hello, John!
bye("John"); // Bye, John!

console.log("Hello, JS-App 101-external");

sayHi("Ade");
```

---

JavaScript Handling form submission with JavaScript

Prevent Default

The preventDefault() method of the Event interface tells the user agent that if the event does not get explicitly handled, its default action should not be taken as it normally would be.

The event continues to propagate as usual, unless one of its event listeners calls stopPropagation() or stopImmediatePropagation(), either of which terminates propagation at once.

As noted below, calling preventDefault() for a non-cancelable event, such as one dispatched via EventTarget.dispatchEvent(), without specifying cancelable: true has no effect.

```javascript
const checkbox = document.querySelector("#id-checkbox");

checkbox.addEventListener("click", checkboxClick, false);

function checkboxClick(event) {
  const warn = "preventDefault() won't let you check this!\n";
  document.getElementById("output-box").innerText += warn;
  event.preventDefault();
}
```

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
todoList.addEventListener("click", (e) => {
  // Delete todo
  if (e.target.classList.contains("delete-btn")) {
    e.target.parentNode.remove();
    saveTodos(getAllTodos());
  }
});
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

```
create directory -  mkdr new-project
enter project directory- cd new-project
create package json-  npm init -y
install the bundler vite as a dev dependencies- npm i --save dev vite
install project files- touch.index{html,CSS,js}
set up git ignore- g ignore node >> .gitignore
set up scripts in the package.json file(dev: Vite, Build: Vite Build & Preview: Vite Preview)
start the project npm run dev

```

The Short Process

```
Initialize Vite- npm create vite @latest new-project
select framework
Enter project directory - cd new-project
start project- npm install & npm run dev

```

---

=======
JavaScript Handling form submission with JavaScript

Prevent Default

The preventDefault() method of the Event interface tells the user agent that if the event does not get explicitly handled, its default action should not be taken as it normally would be.

The event continues to propagate as usual, unless one of its event listeners calls stopPropagation() or stopImmediatePropagation(), either of which terminates propagation at once.

As noted below, calling preventDefault() for a non-cancelable event, such as one dispatched via EventTarget.dispatchEvent(), without specifying cancelable: true has no effect.

```javascript
const checkbox = document.querySelector("#id-checkbox");

checkbox.addEventListener("click", checkboxClick, false);

function checkboxClick(event) {
  const warn = "preventDefault() won't let you check this!\n";
  document.getElementById("output-box").innerText += warn;
  event.preventDefault();
}
```

---

# Summary Of LMS Month 2 week 4.

# FROM PURE JAVASCRIPT TO REACT

the strange function breakdown

below is the strange function, explained.

```js
Type of strange function:  Arrow Function

const makeElem = (elemType, props, children) => {
  const elem = document.createElement(elemType)

  if (props) {
    for (const [key, value] of Object.entries(props)) {
      if (key === 'onclick' && props['once']) {
        elem.addEventListener('click', value, { once: true })
      } else {
        elem[key] = value
      }
   }
  }

  if (children) {
    elem.prepend(...children)
  }

  return elem
}


```

---

# 3 METHOD TO ADD EVENTS

1. html attributes (props)
2. DOM properties
3. add event listeners

note: there are somethings that are not attributes but DOM Event listeners

```js
if (children) {
  elem.prepend(...children);
}
// key thing to note here in this code:
// the element we are creating will serve as the PARENT , and anything inside the (children) will be children

makeElem("h1", {}, []);
//  h1 is element name (parent)
// {      }  is the object (props)
//  [      ]  is the children
```

---

# FURTHER BREAK-DOWN OF THE STRANGE FUNCTION

the function is divided into 4 segment

```js
const makeElem = (elemType, props, children) => {
  const elem = document.createElement(elemType); // first segment

  if (props) {
    for (const [key, value] of Object.entries(props)) {
      if (key === "onclick" && props["once"]) {
        elem.addEventListener("click", value, { once: true });
      } else {
        elem[key] = value;
      }
    }
  } //2nd segment

  if (children) {
    elem.prepend(...children);
  } //3rd segment

  return elem;
}; //4th segment
```

---

```js
/*
in this strange function
2nd segment: quite challenging
3rd segment: simple
4th segment : return
note: every function have a return statement. this means you are returning the element that was created*/
```

<br>

# FURTHER BREAKDOWN ON 2ND SEGMENT

if props is false, the function will skip segment 2
buh if props is true, it will run the FOR loop

<br>

# TYPES OF FOR LOOP

1. FOR OF
2. FOR IN

FOR OF - used with [arrays] and anything that is iterable <br>
FOR IN - used with objects

but, we can use the FOR OF with objects as well

---

# HOW TO CONVERT OBJECT TO AN ARRAY

```js
we use Object.entries(  )


```

<br>

<b>DEFINITION OF ITERABLE:</b>
This is anything that has length and that you can loop through

<br>

# THE GOAL OF THE FOR-OF LOOP IN SEGMENT 2

the goal: is just to give us a key and value for each thing in the object

<br>

# OBJECT/ARRAY/FUNCTION PARAMETER DIS-STRUCTURING

This means where the array/object/function parameters have a structure before, we dis-structure it i.e(plugging somethings out)

---

```js
focusing on Array dis-structuring:


since eachProp is an array and we want to disstructure it ,
in place of eachProp it will be replaced to [variableA, variableB]
OR
[key, value]

note: why we are able to dis-structure the `eachProp, is because it is an array
if it were to be an object,  where we used [   ],  it will be {   }
```

<br>

```js
another example:
document.createElement('p') // putting p into a variable called p

let p= document.createElement('p')

for (let [key, value] of p) //this wont work

for (let [key, value] of dir(p)) // this wont work either
```

---

Now, because p is an element, it is not possible to extract it out atall
so therefore, p is not iterable.

it is when it is been converted to DOM that is when it can behave like an object

technically, element are elements!, it is that cross pollination into a DOM behavior that makes it behave like an object.
outside that cross pollination into a DOM region, you cannot make an element behave like an object

using like, p.style / p.class that it becomes a DOM

```js
EXAMPLE
let h1 = document.createElement('h1')
h1.style= 'color:red;'
color: is key
red:  is value
```

so it's either we use dot notation or square bracket [ ] to make the element behave like an object

```js
elem.addEventListener; //- behaves like an element
elem[key] = value; // - behaves like a DOM
elem.prepend(...children); // - behaves like a DOM
```
