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

# h1 Heading
## h2 Heading
### h3 Heading
#### h4 Heading
##### h5 Heading
###### h6 Heading


## Horizontal Rules

___

---

***


## Emphasis

**This is bold text**

__This is bold text__

*This is italic text*

_This is italic text_

~Strikethrough~~


## Blockquotes


> Blockquotes can also be nested...
>> ...by using additional greater-than signs right next to each other...
> > > ...or with spaces between arrows.


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
3. Integer molestie lorem at massa


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


## Links

[link text](http://dev.nodeca.com)

[link with title](http://nodeca.github.io/pica/demo/ "title text!")

Autoconverted link https://github.com/nodeca/pica (enable linkify to see)


## Images

![Minion](https://octodex.github.com/images/minion.png)
![Stormtroopocat](https://octodex.github.com/images/stormtroopocat.jpg "The Stormtroopocat")

Like links, Images also have a footnote style syntax

![Alt text][id]

With a reference later in the document defining the URL location:

[id]: https://octodex.github.com/images/dojocat.jpg  "The Dojocat"

