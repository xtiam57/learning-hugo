---
title: Learning Hugo
description: We are learning HUGO
date: 2020-09-17T16:59:56-05:00
draft: true
---

# This is a title

This is my first post with HUGO!

```json
{
  name: "string",
  day: 86400,
  hour: 3600,
  minute: 60,
  second: 1 // un segundo tiene... un segundo :D
}
```

```javascript
function foo() {
  // Do stuff
  return true;
}

const DATE_UNITS = {
  name: "string",
  day: 86400,
  hour: 3600,
  minute: 60,
  second: 1 // un segundo tiene... un segundo :D
}

const getSecondsDiff = (timestamp) => {
  // restamos el tiempo actual al que le pasamos por parámetro
  // lo dividimos entre 1000 para quitar los milisegundos
  return (Date.now() - timestamp) / 1000
}
```

```html
<h1 class="foo">Hola</h1>
```

```css
.foo {
  background-color: red;
}
```

```jsx
export default function Foo() {
  return (
    {/* Comments */}
    <div onClick={handleClick}>Some content</div>
  )
}
```
