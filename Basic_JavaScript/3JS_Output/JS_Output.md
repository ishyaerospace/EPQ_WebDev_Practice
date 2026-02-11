# JavaScript Output

## Different Display Possibilities

* writing to html element
    + innerHTML 
    + innerText
* writing to html output
    + Document.write()
* writing into an alert box
    + window.alert()
* writing to browser console
    + Console.log()


## innerHTML

used to change HTML element

access HTML element --> `document.getElementByID(id)`

id is the attribute to identify the HTML element

then use .innerHTML to change the HTML content

see JS_innerHTML.html


## innerText

used to change the plain text

access HTML element --> `document.getElementbyID(id)`
then use .innerText property to change the inner text of the HTML element

see JS_innerText.html

## Document.Write()

for testing use document.write()

using document.write() after an HTML document is loaded will delete all existing HTML

see JS_write.html

## window.alert()

alert box can display data

specifying the window keyword is optional as window object is the global scope object

see JS_alert.html

## console.log()

for debugging purposes, calling console.log() in browser can display data

see JS_consoleLog.html

## print()
Javascript does not have a print object or method
you cannot access output devices from JavaScript

The only exeception is calling window.print() method in the browser to print the content of the current window

see JS_print.html

