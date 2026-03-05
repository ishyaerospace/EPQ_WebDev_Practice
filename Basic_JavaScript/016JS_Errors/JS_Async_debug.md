# debug Async code

async code is the hardest to debug for beginner programmers. the code may look correct but nothing seems to happen.

reasons as to why async code is hard to debug:
async code runs later. this makes errors feel invisible. Common begineer problems include missing data and silent failures.

async code does not run top to bottom, it runs when something finishes.

## debugging fetch()
the fetch() function is asynchronous, it does not return data immediately.

`fetch("data.json")`
`.then(response => response.json())`
`.then(data => console.log(data));`

if nothing appears, check the console first. Always log response before using the data.
the improved debugging code:

`fetch("data.json")`
`.then(response =>{`
`    consol.log(response);`
`    return response.json();`
`})`
`.then(data => console.log(data));`

## network problems
async bugs often are network problems. network tab shows if request failed.
* check the request status
* check the file path
* check if the server returned an error

## debugging async and await
async and await make async code easier to read

`async function loadData() {`
`  let response = await fetch("data.json");`
`  let data = await response.json();`
`  console.log(data);`
`}`

`loadData();`

you can set break points on await lines, then step through async code the same way as normal code

## handling async errors
async errors must be handled explictly, otherwise they fail silently


`async function loadData() {`
`  try {`
`    let response = await fetch("wrong.json");`
`    let data = await response.json();`
`    console.log(data);`
`  } catch (error) {`
`    console.error(error);`
`  }`
`}`

errors inside async functions need to be caught.

