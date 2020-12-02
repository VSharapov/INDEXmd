# INDEX.md

- The idea: project boilerplate - `index.html`
	- No fluff - minimal but not minifed
	- [Dark theme](https://gist.github.com/VSharapov/1405184e3e4005425e9ab0750c2060fe), otherwise default browser style
	- Renders `./README.md` to HTML

## How to add this to your repo:

Just save [this `.html` file](https://raw.githubusercontent.com/VSharapov/INDEXmd/master/index.html) to your repo's directory

---

- The implamentation:
	- Set up sample `README.md` from [https://dillinger.io/](https://dillinger.io/)
	- Going to try using [https://github.com/showdownjs/showdown](https://github.com/showdownjs/showdown) - [http://demo.showdownjs.com/](http://demo.showdownjs.com/)
		- `https://cdn.rawgit.com/showdownjs/showdown/<version tag>/dist/showdown.min.js`
		- [https://cdn.rawgit.com/showdownjs/showdown/1.9.1/dist/showdown.min.js](https://cdn.rawgit.com/showdownjs/showdown/1.9.1/dist/showdown.min.js)
	- Cool, it works, now minimal code to get `./README.md` via [XMLHttpRequest](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest/Using_XMLHttpRequest)
	- Beautiful! But the table doesn's work, is it standard?
		- Not standard, easy to enable: `var converter = new showdown.Converter({'tables': true});`
	- Pruned everything
	- Cleaned up JS
	- Set `document.title` to first element contents
	- I think it's done
	- Replaced sample 
		- [https://github.com/markdown-it/markdown-it/blob/1ad3aec2041cd2defa7e299543cc1e42184b680d/support/demo_template/sample.md](https://github.com/markdown-it/markdown-it/blob/1ad3aec2041cd2defa7e299543cc1e42184b680d/support/demo_template/sample.md)
		- Pruned out plugins and extensions

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
