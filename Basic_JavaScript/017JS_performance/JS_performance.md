# JavaScript Performance

## reduce activity in loops
each statement in a loop and its "for statement" is executed for each iteration of the loop.
statements or assignments can be placed outside the loop to make the loop run faster

bad example:
`for (let i = 0; i < arr.length; i++){`
`    action`
`}`

good example:
`let length = arr.length;`
` for (let i = 0; i < length; i++){`
`    action`
`}`

## reduce DOM access
accessing HTML DOM is very slow compared to other JS statements. if you expect that DOM will be accessed multiple times then save it into a local variable and then modify using the variable:

`const obj = document.getElementById("demo");`
`obj.innerHTML = "Hello";`

## unnecessary variables
dont create new variables if you dont plan to save values.


## delaying JS loading
putting Scripts at the bottom of the page body lets the browser load the page first.
while the script is downloading, the browser will not start any other downloads. in addition all parsing and rendering activity might be blocked.

alternative is to use `defer="true"` in the script tag to tell the browser that the script should be executed after the page has finished parsing, but this only works for external scripts.

