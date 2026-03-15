# JavaScript promises

makes asynchronous JS easier. promise is an object that represents the completion or failure of an asynchronous operation
A promise can be in one of three states:
* pending --> operation started (not yet finished).
* rejected --> operation failed.
* fulfilled --> operation completed.

promise acts as a placeholder for a value that will be available at some point in the future, allowing you to handle asynchronous code in a cleaner way than traditional callbacks

## creating a promise
syntax:
`let myPromise = new Promise(function(resolve, reject){ //first is the resolve second arguament is the reject.`
    
`    // code that will take some time`

`    resolve(value); // function to run if finishes successfully`
`    reject(value); // function to run if finishes with an error`
`});`

## promises how to

how to use a Promise:
`myPromise.then(function(value) {code if successful}, function(value) {code if error})`

then() takes two arguments, callback function for success and callback function for failure. these are optional.

## how promises are represented

myPromise.state           |  myPromise.result
"pending"                 |  undefined
"fulfilled"               |  a result value
"rejected"                |  an error object

## core methods and usage
* .then(onFulfilled, onRejected):
    * attaches handlers for both the fulfillment and rejection cases. it returns a new promise. which enables method chaining.
* .catch(onRejected):
    * shorthand for .then(null, onRejected) --> handles errors at the end of the promise chain
* .finally(onFinally):
    * handler is called when the promise is settled (either fulfilled or rejected) --> useful for cleanup process

`let promise = Promise.resolve("OK");`

`promise`
`.then(function(value) {`
`  console.log(value);`
`})`
`.catch(function(value) {`
`  myDisplayer(value);`
`});`

when promise is fulfilled, the then() function runs.

## promise and real JS
many web APIs return promises, fetch() is a common example

`fetch("data.json")`
`.then(function(response){`
`    return response.json();`
`})`
`.then(function(data){`
`    console.log(data);`
`})`
`.catch(function(error){`
`    console.log(error);`
`})`

## promise API static methods
JS also provides stateic methods on the promise object for handling multiple methods at once:
* Promise.all(iterable):
    - fulfills when all promises in the iterable are fulfilled; rejects immediately if any promise rejects
* Promise.allSettled(iterable):
    - wait for all promises to settle (either fulfilled or reject) and returns an array of their results.
* Promise.race(iterable):
    - settles (fulfills or rejects) as soon as any of the promises in the iterable settles
* Promise.any(iterable):
    - fulfills as soon any promise in the iterable

## waiting for file example
`function getFile(myCallback) {`
`  let req = new XMLHttpRequest();`
`  req.open('GET', "mycar.html");`
`  req.onload = function() {`
`    if (req.status == 200) {`
`      myCallback(req.responseText);`
`    } else {`
`      myCallback("Error: " + req.status);`
`    }`
`  }`
`  req.send();`
`}`

`getFile(myDisplayer);`

