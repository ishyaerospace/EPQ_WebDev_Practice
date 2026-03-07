# HTML DOM

## The DOM tree
when web pages loads, the browser creates a tree like representation of the HTML document
each part of the document is a Node in the tree

NODES:
Document = ownser of all nodes in the document
<html> = Element Node
<head> = Element Node
<body> = Element Node
<a> = Element node
<h1> = Element Node
href = Atrribute Node
My Header = Text Node

## Accessing HTML Elements
The HTML DOM can be used to access HTML elements
the most common way to access this is to use the `id` of the element

`<html>`
`<body>`

`<p id="demo"></p>`

`<script>`
`// Access a paragraph Element`
`const myPara = document.getElementById("demo");`

`// Change the content of the Element`
`myPara.innerHTML = "Hello World!";`
`</script>`

`</body>`
`</html>`

in the example above the `getElementById` method used `id="demo"` to find the element

* `id = "demo" `is an HTML property
* `getElementById()` is a DOM method
* `innerHTML` is a DOM property

