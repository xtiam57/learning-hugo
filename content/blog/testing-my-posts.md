---
title: Guía de estilos del Blog
description: "Descripción del post de prueba..."
image: /images/asset-6.jpeg
summaryType: "wide"
caption: Publicado en **Unplash**
date: 2020-09-17T16:59:56-05:00
draft: true
toc: false
tags:
  - testing
  - hugo
  - draft
  - style guide
categories:
  - Post de prueba
  - Categoría de prueba
---

In maximus dictum turpis, vel suscipit tortor. Nam ut purus sit amet nisi tincidunt pharetra id vitae nunc. Donec blandit ipsum turpis, in ultricies libero ullamcorper eget. Pellentesque blandit aliquam maximus.

## Image Gallery

In maximus dictum turpis, vel suscipit tortor. Nam ut purus sit amet nisi tincidunt pharetra id vitae nunc. Donec blandit ipsum turpis, in ultricies libero ullamcorper eget. Pellentesque blandit aliquam maximus.

{{< gallery columns="3 1 3" heights="1 0.333 1" caption="UIn maximus **dictum turpis**, vel suscipit tortor. Nam ut purus sit amet [link text](http://dev.nodeca.com) nisi tincidunt." >}}
/images/asset-3.jpeg
/images/asset-0.jpeg
/images/asset-1.jpeg
/images/asset-2.jpeg
/images/asset-4.jpeg
/images/asset-5.jpeg
/images/asset-6.jpeg
{{< /gallery >}}

In molestie nisl at est facilisis, sit amet egestas neque volutpat. Cras ut iaculis dolor. Interdum et malesuada fames ac ante ipsum primis in faucibus. In maximus dictum turpis, vel suscipit tortor. Nam ut purus sit amet nisi tincidunt pharetra id vitae nunc. Donec blandit ipsum turpis, in ultricies libero ullamcorper eget. Pellentesque blandit aliquam maximus.

### Another gallery

Donec blandit ipsum turpis, in ultricies libero ullamcorper eget. Pellentesque blandit aliquam maximus.

{{< gallery caption="UIn maximus **dictum turpis**, vel suscipit tortor. Nam ut purus sit amet [link text](http://dev.nodeca.com) nisi tincidunt." >}}
/images/align-left.jpg
/images/align-right.jpg
{{< /gallery >}}

## Columns

In molestie nisl at est facilisis, sit amet egestas neque volutpat. Cras ut iaculis dolor. Interdum et malesuada fames ac ante ipsum primis in faucibus.

{{< columns >}}
### 1st column
Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
tempor incididunt ut labore et dolore magna aliqua.
***
### 2nd column
Duis aute irure dolor in reprehenderit in voluptate velit esse
cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non.
{{< /columns >}}

#### With alignment

We can use class ``class="align-items-start"``, ``class="align-items-center"`` or ``class="align-items-end"``.

In molestie nisl at est facilisis, sit amet egestas neque volutpat. Cras ut iaculis dolor. Interdum et malesuada fames ac ante ipsum primis in faucibus.

{{< columns class="align-items-center" >}}
{{< figure src="/images/test.jpg" >}}
Duis aute irure dolor in reprehenderit in voluptate velit esse
cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non.
***
### 2nd column
Nulla condimentum nibh ac felis molestie commodo. Curabitur eu urna feugiat, molestie est sit amet, mollis nisl. Cras sit amet semper augue. Vivamus rutrum condimentum odio, eget pulvinar nibh posuere non. Nunc purus ipsum, tincidunt vitae metus eget, tristique sollicitudin neque. Aliquam at massa imperdiet, faucibus metus vel, eleifend mauris. Nunc pulvinar accumsan est ut sa
{{< /columns >}}

Nulla condimentum nibh ac felis molestie commodo. Curabitur eu urna feugiat, molestie est sit amet, mollis nisl. Cras sit amet semper augue. Vivamus rutrum condimentum odio, eget pulvinar nibh posuere non. Nunc purus ipsum, tincidunt vitae metus eget, tristique sollicitudin neque. Aliquam at massa imperdiet, faucibus metus vel, eleifend mauris. Nunc pulvinar accumsan est ut sagittis. Praesent vitae justo non erat finibus condimentum. Donec finibus hendrerit nisl, sit amet laoreet est aliquet ut.

## Horizontal Rules

Like this `using _`:
___

Or this `using -`:

---

Or this `using *`:

***

Ut lacinia sapien non lacus aliquet, et molestie est consequat. Vivamus et leo lacus. Mauris egestas luctus ligula, non ultricies elit efficitur quis. Vestibulum et orci nisl. Aliquam ex justo, lobortis eget lacinia vel, luctus ut arcu. Nam ut tempus est. Quisque fringilla purus ut pharetra vehicula. Phasellus eros nulla, fermentum in dictum in, eleifend ac sem. Nam rutrum ipsum ut dui finibus, id maximus diam mollis. Donec eget purus ipsum. Praesent vel rutrum diam, at rutrum eros. Nullam finibus tristique lectus, quis porta elit euismod et. In et euismod nisl, venenatis tristique tellus.

## Code

Inline `code`. We are going to use ``title`` as the caption.

Indented code

    // Some comments
    line 1 of code
    line 2 of code
    line 3 of code


Block code "fences"

```
Sample text here...
```

Syntax highlighting

``` js
var foo = function (bar) {
  return bar++;
};

console.log(foo(5));
```

JSON code example:

```json
{
  "name": "string",
  "day": 86400,
  "hour": 3600,
  "minute": 60,
  "second": 1 // un segundo tiene... un segundo :D
}
```

Javascript large code code example:

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

HTML code example:

```html
<h1 class="foo">Hola</h1>
```

CSS code example:

```css
.foo {
  background-color: red;
}
```

React JSX code example:

```jsx
export default function Foo() {
  return (
    {/* Comments */}
    <div onClick={handleClick}>Some content</div>
  )
}
```

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean id orci id risus aliquet blandit. Suspendisse dapibus ligula id massa gravida, at pellentesque ex efficitur. Praesent tempus lacus eget est condimentum volutpat. Nullam sed pellentesque ipsum, ac bibendum diam. Phasellus at nulla consectetur, interdum lectus a, semper lectus. Fusce ac risus urna. Curabitur et justo eu arcu ultrices suscipit. Proin vel ullamcorper mauris. Phasellus congue lectus sit amet augue lobortis vestibulum. Curabitur est tellus, aliquet id vulputate a, tincidunt ut ante.

{{< pen id="RwRaJWy" tab="js,result" >}}

Nulla condimentum nibh ac felis molestie commodo. Curabitur eu urna feugiat, molestie est sit amet, mollis nisl. Cras sit amet semper augue. Vivamus rutrum condimentum odio, eget pulvinar nibh posuere non. Nunc purus ipsum, tincidunt vitae metus eget, tristique sollicitudin neque. Aliquam at massa imperdiet, faucibus metus vel, eleifend mauris. Nunc pulvinar accumsan est ut sagittis. Praesent vitae justo non erat finibus condimentum. Donec finibus hendrerit nisl, sit amet laoreet est aliquet ut.


## Emphasis

**This is bold text**

__This is bold text__

*This is italic text*

_This is italic text_

~~Strikethrough~~

## Alignment

Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Morbi commodo, ipsum sed pharetra gravida, orci magna rhoncus neque, id pulvinar odio lorem non turpis.

{{< align "left" >}}
> The first thing to do is to look at the table of components for MDX, and here we can see that images are represented by img. By following the link we can see the markdown
>
> <cite>Benjamin Franklin</cite>
{{< /align >}}

Sed tincidunt eget enim et finibus. Nam pulvinar lorem sit amet pulvinar mattis. Curabitur massa tellus, molestie et augue ac, rutrum cursus diam. Curabitur convallis dictum nibh, eget ultrices elit elementum id. Sed quis facilisis est. Curabitur tellus lorem, tempus quis enim sit amet, venenatis malesuada urna. Proin ac metus sed urna vehicula elementum. Etiam congue in lectus at elementum. Ut consequat non felis sit amet pretium.

Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Morbi commodo, ipsum sed pharetra gravida, orci magna rhoncus neque, id pulvinar odio lorem non turpis. Nullam sit amet enim. Suspendisse id velit vitae ligula volutpat condimentum. Aliquam erat volutpat. Sed quis velit. Nulla facilisi. Nulla libero. Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Morbi commodo, ipsum sed pharetra gravida, orci magna rhoncus neque, id pulvinar odio lorem non turpis.

{{< align "left" >}}
{{< figure src="/images/align-left.jpg" >}}
{{< /align >}}

Sed tincidunt eget enim et finibus. Nam pulvinar lorem sit amet pulvinar mattis. Curabitur massa tellus, molestie et augue ac, rutrum cursus diam. Curabitur convallis dictum nibh, eget ultrices elit elementum id. Sed quis facilisis est. Curabitur tellus lorem, tempus quis enim sit amet, venenatis malesuada urna. Proin ac metus sed urna vehicula elementum. Etiam congue in lectus at elementum. Ut consequat non felis sit amet pretium.

Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Morbi commodo, ipsum sed pharetra gravida, orci magna rhoncus neque, id pulvinar odio lorem non turpis. Nullam sit amet enim. Suspendisse id velit vitae ligula volutpat condimentum. Aliquam erat volutpat. Sed quis velit. Nulla facilisi. Nulla libero. Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Morbi commodo, ipsum sed pharetra gravida, orci magna rhoncus neque, id pulvinar odio lorem non turpis.

Sed quis facilisis est. Curabitur tellus lorem, tempus quis enim sit amet, venenatis malesuada urna. Proin ac metus sed urna vehicula elementum. Etiam congue in lectus at elementum. Ut consequat non felis sit amet pretium.

{{< align "right" >}}
{{< figure src="/images/align-right.jpg" >}}
{{< /align >}}

Nam pulvinar lorem sit amet pulvinar mattis. Curabitur massa tellus, molestie et augue ac, rutrum cursus diam. Curabitur convallis dictum nibh, eget ultrices elit elementum id. Sed quis facilisis est.

Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Morbi commodo, ipsum sed pharetra gravida, orci magna rhoncus neque, id pulvinar odio lorem non turpis. Nullam sit amet enim. Suspendisse id velit vitae ligula volutpat condimentum. Aliquam erat volutpat.

Sed quis velit. Nulla facilisi. Nulla libero. Lorem ipsum dolor sit amet, consectetuer adipiscing elit.

Morbi commodo, ipsum sed pharetra gravida, orci magna rhoncus neque, id pulvinar odio lorem non turpis. Sed quis facilisis est. Curabitur tellus lorem, tempus quis enim sit amet, venenatis malesuada urna. Proin ac metus sed urna vehicula elementum. Etiam congue in lectus at elementum. Ut consequat non felis sit amet pretium.

## Blockquotes

> Sed tincidunt eget enim et finibus. Nam pulvinar lorem sit amet pulvinar mattis...

With cite:

> The first thing to do is to look at the table of components for MDX, and here we can see that images are represented by img. By following the link we can see the markdown
>
> <cite>Benjamin Franklin</cite>

## Lists <a id="chapter-1"></a>

Unordered

+ Create a list by starting a line with `+`, `-`, or `*`
+ Sub-lists are made by indenting 2 spaces:
  - Marker character change forces new list start:
    * Ac tristique libero volutpat at
    + Facilisis in pretium nisl aliquet
    - Nulla volutpat aliquam velit
+ Very easy!

Ordered

1. Lorem ipsum dolor sit amet
2. Consectetur adipiscing elit
1. Integer molestie lorem at massa
1. You can use sequential numbers...
1. ...or keep all the numbers as `1.`

Start numbering with offset:

57. foo
1. bar

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean id orci id risus aliquet blandit. Suspendisse dapibus ligula id massa gravida, at pellentesque ex efficitur. Praesent tempus lacus eget est condimentum volutpat. Nullam sed pellentesque ipsum, ac bibendum diam. Phasellus at nulla consectetur, interdum lectus a, semper lectus.

{{< hero >}}
## A title for a great hero
Lorem ipsum dolor sit amet, consectetur adipiscing elit. **Aenean id orci id risus aliquet blandit**. Suspendisse dapibus ligula id massa gravida, at pellentesque ex efficitur. Praesent tempus lacus eget est condimentum volutpat. Nullam sed pellentesque ipsum, ac bibendum diam. _Phasellus at nulla consectetur, interdum lectus a, semper lectus_.
{{< /hero >}}

Fusce ac risus urna. Curabitur et justo eu arcu ultrices suscipit. Proin vel ullamcorper mauris. Phasellus congue lectus sit amet augue lobortis vestibulum. Curabitur est tellus, aliquet id vulputate a, tincidunt ut ante.

## Tables <a id="chapter-2"></a>

| Option | Description |
| ------ | ----------- |
| data   | path to data files to supply the data that will be passed into templates. |
| engine | engine to be used for processing templates. Handlebars is the default. |
| ext    | extension to be used for dest files. |

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean id orci id risus aliquet blandit. Suspendisse dapibus ligula id massa gravida, at pellentesque ex efficitur. Praesent tempus lacus eget est condimentum volutpat. Nullam sed pellentesque ipsum, ac bibendum diam. Phasellus at nulla consectetur, interdum lectus a, semper lectus. Fusce ac risus urna. Curabitur et justo eu arcu ultrices suscipit. Proin vel ullamcorper mauris. Phasellus congue lectus sit amet augue lobortis vestibulum. Curabitur est tellus, aliquet id vulputate a, tincidunt ut ante.

## Figures

Curabitur et justo eu arcu ultrices suscipit. Proin vel ullamcorper mauris. Phasellus congue lectus sit amet augue lobortis vestibulum. Curabitur est tellus, aliquet id vulputate a, tincidunt ut ante.

{{< figure src="/images/full.jpg" class="full" caption="UIn maximus **dictum turpis**, vel suscipit tortor. Nam ut purus sit amet [link text](http://dev.nodeca.com) nisi tincidunt." >}}

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean id orci id risus aliquet blandit. Suspendisse dapibus ligula id massa gravida, at pellentesque ex efficitur. Praesent tempus lacus eget est condimentum volutpat. Nullam sed pellentesque ipsum, ac bibendum diam. Phasellus at nulla

{{< figure src="/images/wide.jpg" caption="UIn maximus **dictum turpis**, vel suscipit tortor. Nam ut purus sit amet [link text](http://dev.nodeca.com) nisi tincidunt." class="wide" >}}

Praesent tempus lacus eget est condimentum volutpat. Nullam sed pellentesque ipsum, ac bibendum diam. Phasellus at nulla

{{< figure src="/images/map.png" caption="UIn maximus **dictum turpis**, vel suscipit tortor. Nam ut purus sit amet [link text](http://dev.nodeca.com) nisi tincidunt."  >}}

Nulla condimentum nibh ac felis molestie commodo. Curabitur eu urna feugiat, molestie est sit amet, mollis nisl. Cras sit amet semper augue. Vivamus rutrum condimentum odio, eget pulvinar nibh posuere non. Nunc purus ipsum, tincidunt vitae metus eget, tristique sollicitudin neque. Aliquam at massa imperdiet, faucibus metus vel, eleifend mauris. Nunc pulvinar accumsan est ut sagittis. Praesent vitae justo non erat finibus condimentum. Donec finibus hendrerit nisl, sit amet laoreet est aliquet ut.

Right aligned columns

| Option | Description |
| ------:| -----------:|
| data   | path to data files to supply the data that will be passed into templates. |
| engine | engine to be used for processing templates. Handlebars is the default. |
| ext    | extension to be used for dest files. |


## Links <a id="chapter-3"></a>

[link text](http://dev.nodeca.com)

[link with title](http://nodeca.github.io/pica/demo/ "title text!")

Autoconverted link https://github.com/nodeca/pica (enable linkify to see)

## Table of Contents
  * [Chapter 1](#chapter-1)
  * [Chapter 2](#chapter-2)
  * [Chapter 3](#chapter-3)

## Images

{{< columns >}}
This is an image with title attribute

![Stormtroopocat](https://octodex.github.com/images/stormtroopocat.jpg "The Stormtroopocat")
***
This is a simple image

![Minion](https://octodex.github.com/images/minion.png)
***
Like links, Images also have a footnote style syntax

![Alt text][id]

With a reference later in the document defining the URL location:

[id]: https://octodex.github.com/images/dojocat.jpg  "The Dojocat"
{{< /columns >}}


### [Emojies](https://github.com/markdown-it/markdown-it-emoji)

Classic markup: :wink: :cry: :laughing: :yum:

### [\<mark>](https://github.com/markdown-it/markdown-it-mark)

<mark>Marked text</mark>

### [Footnotes](https://github.com/markdown-it/markdown-it-footnote)

Footnote 1 link [^first].

Footnote 2 link [^second].

[^first]: Footnote **can have markup** too!
[^second]: Second footnote text.


### [Definition lists](https://github.com/markdown-it/markdown-it-deflist)

Term 1
:   Definition 1
with lazy continuation.

Term 2 with *inline markup*
:   Definition 2

        { some code, part of Definition 2 }

    Third paragraph of definition 2.

### TODO lists

- [x] @mentions, #refs, [links](), **formatting**, and <del>tags</del> supported
- [x] list syntax required (any unordered or ordered list supported)
- [x] this is a complete item
- [ ] this is an incomplete item

