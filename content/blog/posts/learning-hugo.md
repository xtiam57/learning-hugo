---
title: "Learning Hugo: A full example of the article power"
description: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam cursus sapien ipsum, eget egestas urna pulvinar sit amet.
cover: /images/cover4.jpg
date: 2020-09-17T16:59:56-05:00
draft: false
toc: true
---

In maximus dictum turpis, vel suscipit tortor. Nam ut purus sit amet nisi tincidunt pharetra id vitae nunc. Donec blandit ipsum turpis, in ultricies libero ullamcorper eget. Pellentesque blandit aliquam maximus.

In molestie nisl at est facilisis, sit amet egestas neque volutpat. Cras ut iaculis dolor. Interdum et malesuada fames ac ante ipsum primis in faucibus.

# h1 Heading
## h2 Heading
### h3 Heading
#### h4 Heading
##### h5 Heading
###### h6 Heading

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
  name: "string",
  day: 86400,
  hour: 3600,
  minute: 60,
  second: 1 // un segundo tiene... un segundo :D
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

Nulla condimentum nibh ac felis molestie commodo. Curabitur eu urna feugiat, molestie est sit amet, mollis nisl. Cras sit amet semper augue. Vivamus rutrum condimentum odio, eget pulvinar nibh posuere non. Nunc purus ipsum, tincidunt vitae metus eget, tristique sollicitudin neque. Aliquam at massa imperdiet, faucibus metus vel, eleifend mauris. Nunc pulvinar accumsan est ut sagittis. Praesent vitae justo non erat finibus condimentum. Donec finibus hendrerit nisl, sit amet laoreet est aliquet ut.

***

###### Full width figure using shortcode:

```
< figure src="/images/my_image.jpg" caption="My caption" class="full-width" >
```

{{< figure src="/images/cover2.png" caption="UIn maximus dictum turpis, vel suscipit tortor. Nam ut purus sit amet nisi tincidunt." class="full-width" >}}

Sed tincidunt eget enim et finibus. Nam pulvinar lorem sit amet pulvinar mattis. Curabitur massa tellus, molestie et augue ac, rutrum cursus diam. Curabitur convallis dictum nibh, eget ultrices elit elementum id. Sed quis facilisis est. Curabitur tellus lorem, tempus quis enim sit amet, venenatis malesuada urna. Proin ac metus sed urna vehicula elementum. Etiam congue in lectus at elementum. Ut consequat non felis sit amet pretium.

***

## Instagram?

{{< instagram BWNjjyYFxVx hidecaption  >}}

Sed tincidunt eget enim et finibus. Nam pulvinar lorem sit amet pulvinar mattis. Curabitur massa tellus, molestie et augue ac, rutrum cursus diam. Curabitur convallis dictum nibh, eget ultrices elit elementum id. Sed quis facilisis est. Curabitur tellus lorem, tempus quis enim sit amet, venenatis malesuada urna. Proin ac metus sed urna vehicula elementum. Etiam congue in lectus at elementum. Ut consequat non felis sit amet pretium.

## Emphasis

**This is bold text**

__This is bold text__

*This is italic text*

_This is italic text_

~~Strikethrough~~

Sed tincidunt eget enim et finibus. Nam pulvinar lorem sit amet pulvinar mattis. Curabitur massa tellus, molestie et augue ac, rutrum cursus diam. Curabitur convallis dictum nibh, eget ultrices elit elementum id. Sed quis facilisis est. Curabitur tellus lorem, tempus quis enim sit amet, venenatis malesuada urna. Proin ac metus sed urna vehicula elementum. Etiam congue in lectus at elementum. Ut consequat non felis sit amet pretium.

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

```
< hero >Text width markdown< /hero >
```

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

{{< figure src="/images/cover.png" caption="UIn maximus dictum turpis, vel suscipit tortor. Nam ut purus sit amet nisi tincidunt." class="almost-width" >}}

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

# Table of Contents
  * [Chapter 1](#chapter-1)
  * [Chapter 2](#chapter-2)
  * [Chapter 3](#chapter-3)

## Images

| Column 1 | Column 2 |
| ------ | ----------- |
| ![Minion](https://octodex.github.com/images/minion.png)  |  ![Minion](https://octodex.github.com/images/minion.png?width=100px) |
| ![Stormtroopocat](https://octodex.github.com/images/stormtroopocat.jpg "The Stormtroopocat")    |  |

Like links, Images also have a footnote style syntax

![Alt text][id]

With a reference later in the document defining the URL location:

[id]: https://octodex.github.com/images/dojocat.jpg  "The Dojocat"

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

