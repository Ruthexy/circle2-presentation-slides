# <div class="text-20xl text-center text-white">second semester summary</div>
<div class="mt-4 text-2xl text-center text-gray-600">Circle 2 Slides presentation</div>

---

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
```

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

