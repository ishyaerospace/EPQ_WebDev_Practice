# Errors in JavaScript

reference, Type, Range, URI, Sytnax, Eval, Slient errors

## how to handle errors in JavaScript

use try statement to define block of code to be tested for errors while it is being executed
the catch statement allows you to define a block of code to be executed, if an error occurs in the try block.

`try {`
`  Block of code to try`
`} catch(err) {`
`  Block of code to handle errors`
`}`

## reference errors
ReferenceError occurs if a programmer uses a variable that doesnt exist

## Type Errors
Type Errors occurs when a value is of the wrong type or an operation is invalid on that type.
type error can happen if you try to pass a value into something that isnt a function:
`notFunction(5)` will give a typeError.
`num = 1; num.toUpperCase();` will give type error as num.toUpperCase() is not a function

## range error
RangeError occurs when value is outside of range
`new Array(-1)` invalid array length

## URI (Universal Resource Identifier) Error
URIError occurs if an illegal character is used in a URI function
`decodeURI("%%%")` error message: URI malformed

## syntax error
you cannot catch syntax errors as they happen before runtime.


# silent errors
JavaScript will fail silently, JS will run but logical errors will occur.
divide by 0 will not stop the program
accidental assignments rather than comparisons will not stop the program
`let result = "Not Active.";`
`let isActive = false;`

`// Assignment, not comparison`
`if (isActive = true) {` // acidental assignment of isActive. should have been == not =
`  let result = "Active!";`
`}`

numeric operations that fail produce NaN (not an exception)
`const result = parseInt("a"); // wrong data type parsed through`

# finally
finally block executes after the try and catch blocks, wheather an error occured or not. it is commonly used for cleanup tasks.

# throw
throw statement allows programmer to create a custom error. 