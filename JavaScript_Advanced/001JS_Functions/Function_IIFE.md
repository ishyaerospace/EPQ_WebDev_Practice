# IIFE (Immedately Invoked Function Expression)

IIFE is a function that invokes itself. therefore when it is created the complier runs the code immediately. 

Syntax for IIFE:

`(function () {`
`  // Code to run immediately`
`})();`

the above example is a anonymous function as it has no name for the function.
the first brackets are used to tell the compiler that the function should be treated as an expression. (brackets that go around the functiion)
The final brackets are used to tell the compiler to run the function immediately

if you set the function expression to a variable, the return value can be set to the variable.

## arrow functions with IIFE
This example shows arrow notation with arguaments
`((name) => {`
`  let text = "Hello " + name;`
`})("John Doe");`


you can give a name to a IIFE but this is only useful for recusive functions as the name can only be caleed within thw function itself and not globally throughout the program.

