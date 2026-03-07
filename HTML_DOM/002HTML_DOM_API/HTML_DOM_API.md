# HTML DOM API

Application Programming Interface
the DOM API is a set of methods and properties that allow JavaScript to change the content, structure, and style of any HTML elements

API method is an Action that the dev can do on an HTML element.
API porperty is a Value that you can access on a HTML element.

`const myPara = document.getElementById("demo");` // revrieves the "demo" element
`myPara.innerHTML = "Hello World!";` // Change the content of the Element

HTML DOM API abilities
The DOM API provides us with the ability to:
* find and select elements
* change element content and attributes
* add, remove, or modify elements
* change CSS styles
* add event listeners to react to user input

## API methods and properties

Devs use global objects like documents and windows as entry points to any API
if you want to access any element in an HTML page, you always start with accessing the document object. The document object represents the webpage. 

to manipulate HTML with JS you will first need to select an element:
document.getElementById(id) =	Find an element by element id
document.getElementsByTagName(name) = 	Find elements by tag name
document.getElementsByClassName(name) = 	Find elements by class name
document.querySelector(selector) = 	  Find the first element that matches a CSS selector
document.querySelectorAll(selector)= 	Find all elements that match a CSS selector

document object is the ownser of all other objects in the webpage

## accessing Element Content
element.innerHTML = HTML content of an element
element.textContent = Text Content of an element

## Accessing Element attributes
element.attribute = attribute value of HTML element
element.style.property = style of HTML element

## changing Element attributes
element.setAttribute() = create or set a new attribute

## manipulat structure
document.createElement() = create a new HTML element
document.removeChild() = remove an HTML element
document.appendChlid() = add an HTML element
document.replaceChild() = replace an HTML element

## event handlers
document.getElementById(id).onclick = function() = adding event handler code to an onclick event


Element and Document reference -> list of all the properties and methods that can be used on either document or the element.
