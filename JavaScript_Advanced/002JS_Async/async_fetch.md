# JS fetch() API

fetch() is the modern way to request data from a server

fetch() is asynchronous and returns a promise
modern apps use async code to get data
fetch() is most common.

fetch returns a promise (does not return the data) that becomes a response later
`fetch("data.json")`
`.then(function(response) {`
`  console.log(response);`
`});`
response is the object not the json data

## getting JSON Data
to get JSON you need to read the response body.
response.json() returns a promise

this promise chain shows how json can be retrieved.
`fetch("data.json")`
`.then(function(response) {`
`  return response.json();`
`})`
`.then(function(data) {`
`  console.log(data);`
`});`

## fetch with async and await
async and await code:
`async function loadData() {`
`  let response = await fetch("data.json");`
`  let data = await response.json();` // using await gives the data rather than the promise
`  console.log(data);`
`}`

`loadData();`

## HTTP errors
fetch does not fail on 404 or 500, fetch only rejects network errors
A 404 promise is not a rejected promise: you must check response.ok
example:

`async function loadData() {`
`  let response = await fetch("missing.json");`

`  if (!response.ok) {`
`    console.log("HTTP Error:", response.status);`
`    return;`
`  }`

`  let data = await response.json();`
`  console.log(data);`
`}`

`loadData();`

## network errors
network errors happen when the request cannot be completed
includes offline mode and DNS errors
network errors reject the promise

`async function loadData() {`
`  try {`
`    let response = await fetch("data.json");`
`    let data = await response.json();`
`    console.log(data);`
`  } catch (error) {`
`    console.log("Network error");`
`  }`
`}`

