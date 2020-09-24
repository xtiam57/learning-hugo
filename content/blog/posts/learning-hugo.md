---
title: Learning Hugo
description: We are learning HUGO
date: 2020-09-17T16:59:56-05:00
draft: false
---

## This is a title

Using MDX you can overwrite the default components that are provided by markdown. In this blog I will use this to add captions to images.

- [x] One task

{{< instagram BWNjjyYFxVx hidecaption  >}}

Using MDX you can overwrite the default components that are provided by markdown. In this blog I will use this to add captions to images.

- uno
- dos
- tres

```json
{
  name: "string",
  day: 86400,
  hour: 3600,
  minute: 60,
  second: 1 // un segundo tiene... un segundo :D
}
```

The first thing to do is to look at the table of components for MDX, and here we can see that images are represented by img. By following the link we can see the markdown

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

Then we create a React component, where each of the keys are passed inside props

```html
<h1 class="foo">Hola</h1>
```

A conditional statement is used here so that no excess formatting is introduced if no title is present. The standard figure layout is used as a tag is there specifically for captions

You can then pass this component to MDX in the method detailed here and the captions should not display themselves. You can then apply CSS or classes to the HTML tags in order to style it as you want.

```css
.foo {
  background-color: red;
}
```

You can then pass this component to MDX in the method detailed here and the captions should not display themselves. You can then apply CSS or classes to the HTML tags in order to style it as you want.

```jsx
export default function Foo() {
  return (
    {/* Comments */}
    <div onClick={handleClick}>Some content</div>
  )
}
```

You can then pass this component to MDX in the method detailed here and the captions should not display themselves. You can then apply CSS or classes to the HTML tags in order to style it as you want.

o adapt this component, we are going to use ``title`` as the caption.
