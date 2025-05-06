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
callbackEx('Do you have a boyfriend', () => console.log('yes'), () => console.log('no'))
```


---

# Month 2 - Week 1 
# Searching The DOM 

An Element with the id 'app' can be assigned to the element variable in two ways; 

``` ts
const element = document.querySelector('#app')

const element = document.getElementById('app')
```

We search the DOM using document.querySelector or document.getElementById . 
The element.innerHTML property allows us to set the HTML content of an element.

# Changing the DOM
Here, we learnt how to add, remove and update elements in the DOM. We also learnt that Adding HTML Elements, Text, Comments, Attributes, Properties and styles are some of the ways to change the DOM.


---  

# Importing CSS in Javascript 
To do this,
```ts
import "./styles.css";
```

# Adding HTML using innerHTML Property 

```ts
elements.innerHTML =`
   <div>
      Hello There!
    </div>
`;    
```
# Adding Texts and Elements

After creating the element,  we add it to the DOM using appendChild or insertBefore.
Other ways to add elements to the DOM is prepend, append, before and after method.

# Removing Elements from the DOM 
 This is done using the remove method

```
element.remove();
```


---
---
# Update Text
The textContent property allows us to set the text content of an element

# EVENTS
These are actions that happen in a browser that you can listen for and respond to. Like, when you press a key, when you load a page, when you submit a form, when you click a button. These are all events.

We listen for events and respond to them with Event Listeners.

To demonstrate how events works in js using a counter:

```ts
export function setUpCounter(element) {
  let counter=0;

  const setCounter = (count) => {
    counter = count;
    element.innerHTML = `count is ${counter}`;
  };

+    element.addEventListener('click', () => setCounter(counter +1));

    setCounter(0);
}

```





