Resources:
- https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Scripting/Event_bubbling

"Event Bubbling" means events bubbling up a tree of clickable elements (where "clickable" means they have an event listener attached).

Assuming the following html:
```html
<div id="card">
	<button id="button">A button</button>
</div>
```

and the following JS
```js
function handleClick(event) {
  console.log(event.currentTarget.tagName)
}

const container = document.querySelector("#card");
container.addEventListener("click", handleClick);
```

If we click on the `<button>` now, the console will log "DIV". That makes sense because we only have an event listener on the parent div. Now let's also add an event listener to the button:

```js
function handleClick(event) {
  console.log(event.currentTarget.tagName)
}

const container = document.querySelector("#card");
const button = document.querySelector("#button");
container.addEventListener("click", handleClick);
button.addEventListener("click", handleClick);
```

If we click the `<button>` now, the console will log
```
"BUTTON"
"DIV"
```

which means we registered the first click event on the `<button>`, but then _also_ the one on the `<div>`. The **event has bubbled up**.