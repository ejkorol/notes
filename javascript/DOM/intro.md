# Document Object Model

## What is it?

A programming API for HTML, it is represented as a tree-like structure. The browser creates the DOM as it parses HTML. With the document object model we have the ability to add, delete and modify the HTML elements and content.

```
<html>
    <body>
        <h1>Title</h1>
        <p><span>word</span></p>
    </body>
</html>
```

*This gets parsed into:*

```
DOCUMENT
|- ELEMENT: html
|   |- ELEMENT: body
|   |- ELEMENT: '\n'
|   |- ELEMENT: h1
|   |   |- TEXT: 'Title'
|   |- ELEMENT: p
|   |   |- TEXT: 'A'
|   |   |- ELEMENT: span
|   |   |   |- TEXT: 'word'
|   |   |- TEXT: '\n'
|   |- TEXT: '\n'
```

The DOM is the bridge between HTML and CSS, and provides us with methods to manipulate the content within HTML.

## Accessing the DOM

### The defer attribute

When the `script` is placed within the `head` of HTML, the javacript will run in parallel *(simultaneously)* when the HTML is loading.

`<script src="./script.js" defer />`

Will load the javascript ***AFTER*** the browser has finished parsing the HTML.

### Some examples of Selectors

`document.getElementById('some-id')` <- By ID

`document.querySelector('p')` <- by Element
This tries to find an element with a `<p></p>` tag, *only the first occurance*.

`document.querySelectorAll('.alert)` <- All by class

We can change the DOM like this:

```
<h1 id="intro">Some, Text</h1>
document.getElementById('intro').innerText = 'Some, More, Text';
```

*`getElementById` is a method*

### Naming Conventions

As with all naming conventions, whatever you choose should be consistent, meaningful and scalable.

#### Meaningful Names

```
// GOOD
const pageTitle = document.querySelector('title');
```

```
// BAD
const el = document.querySelector('title');
```

#### Naming

```
// CamelCase
const pageTitle = document.querySelector('title');
```

```
// PascalCase
const PageTitle = document.querySelector('title');
```

```
// Snake_case
const page_title = document.querySelector('title');
```

#### Using Prefixes

when you're dealing with DOM elements, you might use a prefix like $ or el to denote that the variable represents an element. This can make your code more readable and help other developers quickly understand the purpose of the variable.

> ### For Elements
> Using the: `$` prefix (for elements)
> `const $pageTitle = document.querySelector('title');`
> 
> (for collections)
> `const $menuItems = document.querySelectorAll('.menu-item');`
>
> Using the `el` prefix:
> `const elHeader = document.querySelector('header');`

### Some more methods

`document.createElement()`
*Creates a new element*

***Element***
`Element.innerHTML`
*The HTML children contents as a string*

`Element.style`
*A map-like collection of the element's styles*

`Element.classList.add()` / `Element.classList.remove()`
*Adds or removes a class from an element*

`Element.getAttribute` / `Element.setAttribute`
*Gets or sets an attribute of the element*

`Element.appendChild`
*Places a child element inside the element*

`Element.append`
*Places a number of multiple elements inside the element*

> Where `Element` is a declaration of a targeted HTML element.

## Creating Elements

```
const divEl = document.createElement('div')
const cardsListEl = document.querySelector('.card-list')

divEl.innerHtml = "<span> Hello Hello </span>"
divEl.classList.add('card')

cardsListEl.append(divEl)
```

## NodeList

> *NodeList is not an array, but has similar methods as an array*

In the Document Object Model (DOM), a NodeList is a collection of nodes. Nodes can be elements, text nodes, comments, etc., that are part of the DOM tree structure. NodeList objects are typically returned by DOM methods such as querySelectorAll() and childNodes.

### NodeList Architecture

```
 NodeList
  ├── Element Node (index: 0)
  ├── Element Node (index: 1)
  └── Element Node (index: 2)
```

### NodeList Method Example

```
CollectionOfElements.childNodes.forEach((childNode) => {
    console.log(childNode)
})
```

*A child Node are elements that exist within a node... Makes sense?*

---

*Lecture: The Document Object Model*
*Date: Friday May 10th, 2024*
