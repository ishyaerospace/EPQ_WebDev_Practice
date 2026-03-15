# JavaSCript async and await

async and await makes promises easier. 
promises are still used however the code is written like normal step by step code.

async makes a function return a promise.
await makes a function wait for a promise.

## existance
promise cahins can become long.
async and await were created to reduce the nesting and improve readability.

promises example:
`// Three functions to run in steps`
`function step1() {`
`  return Promise.resolve("A");`
`}`
`function step2(value) {`
`  return Promise.resolve(value + "B");`
`}`
`function step3(value) {`
`  return Promise.resolve(value + "C");`
`}`

`// Run the three functions in steps`
`step1()`
`.then(function(value) {`
`  return step2(value);`
`})`
`.then(function(value) {`
`  return step3(value);`
`})`
`.then(function(value) {`
`  myDisplayer(value);`
`});`

same code but written with async and await:

`// function to run three function in steps`
`async function run(){`
`    let v1 = await step1();`
`    let v2 = await step2(v1);`
`    let v3 = await step3(v2);`
`    myDisplay(v3);`
`}`

`run();`

## async keyword
the async keyword before a function makes the function return a promise.

`async function myFunction(){`
`    return "hello";`
`}`

is the same as 

`function myFunction(){`
`    return Promise.resolve("hello");`
`}`

after use .then() to make it a proper promise:

`myFunction().then{`
`    function(value) {Code if successful}`
`    function(value) {Code if some error}`
`}`

## await keyword
makes a function pause the execution and wait for a resolved promise before continuing.

`let value = await promise;`

this keyword can only be used inside an async function

## Handling errors with try...catch
Promises use catch() for errors
async and await use try...catch


`function fail() {`
`  return Promise.reject("Failed");`
`}`

`async function run() {`
`  try {`
`    let value = await fail();`
`    console.log(value);`
`  } catch (error) {`
`    console.log(error);`
`  }`
`}`

`run();`

## fetch()
fetch() returns a promise
can be used with await and async

`async function loadData() {`
`  try {`
`    let response = await fetch("data.json");`
`    let data = await response.json();`
`    console.log(data);`
`  } catch (error) {`
`    console.log(error);`
`  }`
`}`

`loadData();`

