# Related Work

This lists other alternatives.

- [mdast](#mdast)
- [md-schema](#md-schema)
- [markdown-to-json](#markdown-to-json)
- [markup-it](#markup-it)
- [md-to-json](#md-to-json)
- [md2json](#md2json)
- [md-to-rdfa](#md-to-rdfa)

## [mdast](https://github.com/syntax-tree/mdast)

> Markdown Abstract Syntax Tree.
>
> mdast is a specification for representing markdown in a syntax tree. It implements unist. It can represent several flavours of markdown, such as CommonMark and GitHub Flavored Markdown.

## [md-schema](https://github.com/f43i4n/md-schema)

First concept notes exist (at <https://github.com/f43i4n/md-schema/tree/master/docs>).
An outline Python implementation exists.

## [markdown-to-json](https://github.com/MoOx/markdown-to-json)

````markdown
---
test: a
test2: b
---

### Test

[link](href)

```js
console.log(window);
```
````

to

```js
{
  "test": "a",
  "test2": "b",
  "headings": [
    {
      "id": "test",
      "level": 2,
      "text": "Test"
    }
  ],
  "body": {
    "tag": "div",
    "children": [
      {
        "tag": "h2",
        "props": {
          "id": "test"
        },
        "children": [
          //...
        ]
      }
    ]
  }
}
```

## [markup-it](https://github.com/GitbookIO/markup-it)

Parses to some XML-tree.

Example: <https://github.com/GitbookIO/markup-it/blob/master/__tests__/__fixtures__/from-markdown/headings/line-h2/output.js>

## [md-to-json](https://www.npmjs.com/package/md-2-json)

> https://github.com/ajithr/md-2-json

### Example

#### Simple content

```js

var md2json = require('md-2-json');

md2json.parse('This is a markdown content');

/* output
{
    raw: "This is a markdown content\n"
}
*/
```

#### Multiline Content

```js

var md2json = require('md-2-json');
var mdContent = `
# Heading 1

This is a para

- This is a list

## Heading 2

This is a para
`

md2json.parse(mdContent);

/* output
{
    "Heading 1": {
        raw: "This is a para\n - This is a list\n",
        "Heading 2": {
            raw: "This is a para\n"
        }
    }
}
*/

```

## [md2json](https://www.npmjs.com/package/@jackens/md2json)

Code repository is 404

## [md-to-rdfa](https://github.com/PatternAtlas/md-to-rdfa)

Converts markdown to RDF-A.

Parses Markdown using pattern matching.
