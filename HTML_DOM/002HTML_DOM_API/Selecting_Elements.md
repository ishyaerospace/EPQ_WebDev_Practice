# Selecting Elements

## Finding HTML elements 

several ways to find elements:
id, tag name, class name, CSS selectors, HTML object collections.

## finding HTML Element by ID
easiest way to find element in DOM
`const element = document.getElementById("intro");`

if element is found, method will return element as an object
if not found, element will contain null


## Finding HTML Element by Tag Name
`const element = document.getElementsByTagName("p");` finds all `<p>` elements

you can find specific IDs that have a certain tag.
`const x = document.getElementById("main");`
`const y = x.getElementsByTagName("p");`
finds element with id="main" and then finds all `<p>` elements inside "main"

## Finding Element by Class Name
`const x = document.getElementsByClassName("intro");`

## finding HTML Elements by CSS Selectors

### QuerySelector() method
gets the first element that has the class. (first match)

`// Access a paragraph Element`
`const myPara = document.querySelector(".demo");`

`// Change the content of the Element`
`myPara.innerHTML = "Hello World!";`

see QuerySelector.html

### QuerySelectorAll() method
this returns a list of all the elements with a specific class or id.

`<p class="demo">One</p>`
`<p class="demo">Two</p>`

`const myItems = document.querySelectorAll(".demo");`

`// Change the content of the Element`
`myItems[0].innerHTML = "First";`

find all HTML elements that match a specified CSS selector (id, class name, types, attributes, values of attributes etc.)

you are able to return a list of all `<p>` elements with `class="intro"`
`const x = document.querySelectorAll("p.intro")`

see QuerySelectorAll.html

