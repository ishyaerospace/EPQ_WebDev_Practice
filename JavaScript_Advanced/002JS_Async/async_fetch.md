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

