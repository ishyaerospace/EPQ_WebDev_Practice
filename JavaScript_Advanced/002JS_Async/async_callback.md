# async callbacks. 

A callback is a function that runs later. callbacks run after something has finished
this was JS first solution for handling asynchronous results that could not immediately be available

## event handling 
callback function is set as an arguament in an event listner
example:
`document.getElementById("myButton").addEventListener("click", displayDate);`

## callback idea

run code after the result is ready. you must give JS a callnback function to call later. 

`function done(value) {`
`  myDisplayer(value);`
`}`

`setTimeout(function() {`
`  done(5);`
`}, 1000);`

this code allows the calculation to be finished before running the display function:

`function myDisplayer(some) {`
`  document.getElementById("demo").innerHTML = some;`
`}`

`function myCalculator(num1, num2, myCallback) {`
`  let sum = num1 + num2;`
`  myCallback(sum);`
`}`

`myCalculator(5, 5, myDisplayer);`

