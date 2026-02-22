# Functions

many of the implementation of functions are similar to python so i will not go indepth

functions can be written in one line
`function sayHello() { return "Hello World"; }`

to call you must use its name with parenthesis.
`let message = sayHello();`

## default parameters

functions can be called with missing arguaments. These missing values are set to undefined. 
sometimes this is acceptable, but sometimes it is better to have default values:

`function myFunction(x, y) {`
`  if (y === undefined) {`
`    y = 2;`
`  }`
`}`

or you can use:

`function myFunction(x, y = 10) {`
`  return x + y;`
`}`

## function rest paramenters

the rest parameter (...) allows a function to treat an indefinite number of arguaments as an array.

`function sum(...args) {`
`  let sum = 0;`
`  for (let arg of args) sum += arg;`
`  return sum;`
`}`

`let x = sum(4, 9, 16, 25, 29, 100, 66, 77);`

## arguaments vs objects
arguaments are passed by value, function only knows the value not the arguament's location so the function does not change the original value in memory.

objects are passed by reference, object references are values, therefore if a function changes an objects property, it changes the original value. 

## function expression
a function is stored in a variable

`const multiply = function(a,b){`
`    return a * b;`
`}`

you can use this to pass functions into parameters of other functions by passing through a variable.
`function run(fn) {`
`  return fn();`
`}`

`const sayHello = function() {`
`  return "Hello";`
`};`

`run(sayHello);`

function expressions are not hoisted so it cannot be called before its defined, whereas function declaration is hoised and therefore it can be called before its defined

## function arrows
acts as the return keyword, removes the return statement and curly brackets
`const add = (a, b) => a * b;`

### arrow function systax
an arrow function uses the => symbol

if the function body only contains one statement you can remove the word function, curly brackets and the return keyword.
`onst add = (a, b) => a * b;`

## arrow functions and "this" keyword
arrow functions do not have their own "this" value.
They inherit "this" from the surrounding code.

`const person = {`
`  name: "John",`
`  greet: function() {`
`    return this.name;`
`  }`
`};`

using the "=>" symbol can have unexpected results and therefore should not be used when using "this".

dont use Arrow Functions:
* as object methods
* when you need your own "this"
* When using function declarations