---
title: Learning Hugo
description: We are learning HUGO
summary: Using MDX you can overwrite the default components that are provided by markdown. In this blog I will use this to add captions to images.
cover: /images/cover.png
date: 2020-09-17T16:59:56-05:00
draft: false
toc: true
---

Using MDX you can overwrite the default components that are provided by markdown. In this blog I will use this to add captions to images.

Using MDX you can overwrite the default components that are provided by markdown. In this blog I will use this to add captions to images.

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

{{< figure src="/images/cover2.png" caption="Using MDX you can overwrite the default components." class="full-width" >}}

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

---
__Advertisement :)__

- __[pica](https://nodeca.github.io/pica/demo/)__ - high quality and fast image
  resize in browser.
- __[babelfish](https://github.com/nodeca/babelfish/)__ - developer friendly
  i18n with plurals support and easy syntax.

You will like those projects!

---

# h1 Heading 8-)
## h2 Heading
### h3 Heading

{{< instagram BWNjjyYFxVx hidecaption  >}}

#### h4 Heading
##### h5 Heading
###### h6 Heading


## Horizontal Rules

___

Hello Moto.

***


## Typographic replacements

Enable typographer option to see result.

{{< hero >}}
A conditional *statement is used here* so that no excess **formatting is introduced** if no title is present. The standard figure layout is used as a tag is there specifically for captions.
{{< /hero >}}

## Emphasis

**This is bold text**

__This is bold text__

*This is italic text*

_This is italic text_

~~Strikethrough~~


## Blockquotes

> Blockquotes can also be nested...

Unordered

> The first thing to do is to look at the table of components for MDX, and here we can see that images are represented by img. By following the link we can see the markdown
>
> <cite>Benjamin Franklin</cite>

## Lists

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



## Code

Inline `code`

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

```c++
var foo = function (bar) {
  return bar++;
};

console.log(foo(5));
```

## Tables

| Option | Description |
| ------ | ----------- |
| data   | path to data files to supply the data that will be passed into templates. |
| engine | engine to be used for processing templates. Handlebars is the default. |
| ext    | extension to be used for dest files. |

Right aligned columns

| Option | Description |
| ------:| -----------:|
| data   | path to data files to supply the data that will be passed into templates. |
| engine | engine to be used for processing templates. Handlebars is the default. |
| ext    | extension to be used for dest files. |


## Links <a id="chapter-1"></a>

[link text](http://dev.nodeca.com)

[link with title](http://nodeca.github.io/pica/demo/ "title text!")

Autoconverted link https://github.com/nodeca/pica (enable linkify to see)

# Table of Contents
  * [Chapter 1](#chapter-1)
  * [Chapter 2](#chapter-2)
  * [Chapter 3](#chapter-3)

## Images

![Minion](https://octodex.github.com/images/minion.png)
![Stormtroopocat](https://octodex.github.com/images/stormtroopocat.jpg "The Stormtroopocat")
![Minion](https://octodex.github.com/images/minion.png?width=100px)
![stormtroopocat](https://octodex.github.com/images/stormtroopocat.jpg?classes=shadow)
![stormtroopocat](https://octodex.github.com/images/stormtroopocat.jpg?classes=border,shadow)
![Minion](https://octodex.github.com/images/minion.png?featherlight=false)

Like links, Images also have a footnote style syntax

![Alt text][id]

With a reference later in the document defining the URL location:

[id]: https://octodex.github.com/images/dojocat.jpg  "The Dojocat"




### [Emojies](https://github.com/markdown-it/markdown-it-emoji)

> Classic markup: :wink: :crush: :cry: :tear: :laughing: :yum:


see [how to change output](https://github.com/markdown-it/markdown-it-emoji#change-output) with twemoji.



### [\<mark>](https://github.com/markdown-it/markdown-it-mark)

<mark>Marked text</mark>


### [Footnotes](https://github.com/markdown-it/markdown-it-footnote)

Footnote 1 link [^first].

Footnote 2 link [^second].

Duplicated footnote reference [^second].

[^first]: Footnote **can have markup**
[^second]: Footnote text.


### [Definition lists](https://github.com/markdown-it/markdown-it-deflist)

Term 1

:   Definition 1
with lazy continuation.

Term 2 with *inline markup*

:   Definition 2

        { some code, part of Definition 2 }

    Third paragraph of definition 2.



- [x] @mentions, #refs, [links](), **formatting**, and <del>tags</del> supported
- [x] list syntax required (any unordered or ordered list supported)
- [x] this is a complete item
- [ ] this is an incomplete item

