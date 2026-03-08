# definitions vs Declarations

function definition is a general term for defining a function
function declaration is one specific way to define a fucntion

## function declaration
`function myFunction(x,y){`
`    return x * y;`
`}`

## function expression (Named)
const myFunction = function name(x,y){
    return x * y;
}

## function expression (Anonymous)
const myFunction = function (x,y){
    return x * y;
}

## arror function
const myFunction = (x,y) => x * y;

## function constructor
const myFunction = new Function("x", "y", "return x * y);

## object method
const obj = {
    myFunction(x,y){
        return x * y;
    }
}

## hoisting
function declaration are hoisted to the top of their scope
function expressions are not hoisted in the same way

function declaration can be called before defined
function expressions cannot be called before they are defined


# Function Callbacks

A callback function is a function passed as an arguament into another function
a callback function is intended to be executed later (specific event occurs or an asynchronous operation completes)

## types of callbacks
asynchronous callbacks:
executed at a later time, allowing the main program to continue to run without waiting, this prevents applications from freezing log-running tasks like network requests <-- inportant for my application

Synchronous callbacks:
executed immediately within the outer fucntion, blocking further operations until completion.

## event handling with callbacks
call backs are oftern used in event handling in JS. user interactions are handled by providing callback functions to an event listener.

`document.getElementById("button").addEventListener("click", displayDate);`

displayDate is the callback function passed as an arguament through the addEventListener() method.
displayDate will be called when the user clicks the button with id "button".

when passing in functions as arguaments DO NOT use parenthesis.

