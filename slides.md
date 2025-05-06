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




<!-- https://sli.dev/guide/animations.html#click-animation -->



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
    elem.prepend(...children)
  }
// key thing to note here in this code: 
// the element we are creating will serve as the PARENT , and anything inside the (children) will be children

makeElem('h1', {         },  [        ] )
//  h1 is element name (parent)
// {      }  is the object (props)
//  [      ]  is the children

```


---

# FURTHER BREAK-DOWN OF THE STRANGE FUNCTION
the function is divided into 4 segment

```js
const makeElem = (elemType, props, children) => {
  const elem = document.createElement(elemType) // first segment

  if (props) {
    for (const [key, value] of Object.entries(props)) {
      if (key === 'onclick' && props['once']) {
        elem.addEventListener('click', value, { once: true })
      } else {
        elem[key] = value
      }
   }
  }  //2nd segment

  if (children) {
    elem.prepend(...children)
  }  //3rd segment

  return elem
} //4th segment



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

# OBJECT/ARRAY/FUNCTION PARAMETER  DIS-STRUCTURING
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

using like, p.style  / p.class that it becomes a DOM

```js 
EXAMPLE
let h1 = document.createElement('h1')
h1.style= 'color:red;'
color: is key
red:  is value
```

so it's either we use dot notation or square bracket [ ] to make the element behave like an object

```js
elem.addEventListener  //- behaves like an element
elem[key] = value      // - behaves like a DOM
elem.prepend(...children) // - behaves like a DOM
```

