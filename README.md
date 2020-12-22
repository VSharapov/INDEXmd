# INDEX.md
A boilerplate `.html` file that renders your `README.md`

## Demo
[https://vsharapov.github.io/INDEXmd/](https://vsharapov.github.io/INDEXmd/)

## How to add this to your repo:

Just save [this `.html` file](https://raw.githubusercontent.com/VSharapov/INDEXmd/master/index.html) to your repo's directory

Stuff you might wanna mess with:

- `fileToRender = 'README.md';`
- `menuOptions` defaults can be changed
    - `readable` is hardcoded to `...maxWidth="70ch";`
- Markdown parser options
    - Before `new showdown.Converter();` e.g. `showdown.setOption('tables', true);`
    - See defaults (and all options) with `console.log(showdown.getOptions());`
- Da🅽k mode: `color: maroon;`

---

---

This a test of all markdown possibilities:

------------------------------------------

## Headings

# h1 Heading 1
## h2 Heading 2
### h3 Heading 3
#### h4 Heading 4
##### h5 Heading 5
###### h6 Heading 6

------------------------------------------

## Horizontal Rules

___

---

***

------------------------------------------

## Emphasis

**This is bold text**

__This is bold text__

*This is italic text*

_This is italic text_

~~Strikethrough~~ (non-spec)

------------------------------------------

## Links

[link text][1]

[link with title][2]

This is [an example](http://example.com/ "Title") inline link.

[This link](http://example.com/) has no title attribute.

------------------------------------------

## Blockquotes

> Blockquotes can also be nested...
>> ...by using additional greater-than signs right next to each other...
> > > ...or with spaces between arrows.

------------------------------------------

## Lists

### Unordered

+ Create a list by starting a line with `+`, `-`, or `*`
+ Sub-lists are made by indenting 4 spaces:
    - Marker character change forces new list start:
        * Ac tristique libero volutpat at
        + Facilisis in pretium nisl aliquet
        - Nulla volutpat aliquam velit
+ Very easy!

### Ordered

#### Numers in sequence

1. Lorem ipsum dolor sit amet
2. Consectetur adipiscing elit
3. Integer molestie lorem at massa

#### Numers not in sequence

1. You can use sequential numbers...
1. ...or keep all the numbers as `1.`

#### Start numbering with offset:

57. foo
1. bar

------------------------------------------

## Images

![Alt text][3]
![Alt text][4]

Like links, Images also have a footnote style syntax

![Alt text][id]

With a reference later in the document defining the URL location:

------------------------------------------

## Tables
(non-spec)

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

------------------------------------------

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

Syntax highlighting (non-spec)

``` js
var foo = function (bar) {
  return bar++;
};

console.log(foo(5));
```

------------------------------------------


[1]: http://example.com/
[2]: http://example.com/ "title text!"
[3]: data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAA0AAAAHCAYAAADTcMcaAAAAOUlEQVQYlWP4TwZg+P///38GBgY4xqkQSY4BWQCZRlGELo/NJnQa3SAGdElcmrDahA9gOBevahwAALsWIux6PC+GAAAAAElFTkSuQmCC
[4]: data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAA0AAAAHCAYAAADTcMcaAAAAOUlEQVQYlWP4TwZg+P///38GBgY4xqkQSY4BWQCZRlGELo/NJnQa3SAGdElcmrDahA9gOBevahwAALsWIux6PC+GAAAAAElFTkSuQmCC "Image title"
[id]: data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAA0AAAAHCAYAAADTcMcaAAAAOUlEQVQYlWP4TwZg+P///38GBgY4xqkQSY4BWQCZRlGELo/NJnQa3SAGdElcmrDahA9gOBevahwAALsWIux6PC+GAAAAAElFTkSuQmCC "Image title"
