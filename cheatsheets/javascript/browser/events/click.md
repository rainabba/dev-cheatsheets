# Click


## Syntax

```javascript
TARGET.onClick = FUNCTION
```

Or

```
TARGET.addEventListener('click', FUNCION)
```

Or directly an HTML element.

```html
<div onClick="foo"></div>

<div onClick="foo('bar')"></div>
```



## Example

e.g. Pick a button or event `document.body` instead and attached a click event.

```javascript
const el = document.body;
// OR
// const el = document.getElementbyId("my-button")

el.addEventListener('click', function(event) {
  console.log('Clicked!')

  console.log(event)
  // e.g. click { target: pre.CodeMirror-line , buttons: 0, 
  //              clientX: 369, clientY: 284, layerX: 60, layerY: 11 }

  console.log(this)
  // e.g. <body class="..." style="...."> ...
})
```

Note how `this` is the element that the click event was attached to.

