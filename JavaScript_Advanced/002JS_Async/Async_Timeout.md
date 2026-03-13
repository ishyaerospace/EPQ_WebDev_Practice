# async Timout

## setTimeout() method
The setTimeout() method schedules a function to run after a delay in milliseconds.
this prevents freezing the browser when running long tasks.

`setTimeout(myFunction, 3000);`

`function myFunction() {`
`  document.getElementById("demo").innerHTML = "Function executed";`
`}`

## setIntervals
setIntervals(function, interval_time_in_ms);

function is ran after every time specified