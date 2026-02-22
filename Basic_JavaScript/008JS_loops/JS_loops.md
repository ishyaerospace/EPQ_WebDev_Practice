# JS loops
able to run same code over and over again with different values.

Instead of writing:
`text += cars[0] + "<br>";`
`text += cars[1] + "<br>";`
`text += cars[2] + "<br>";`
`text += cars[3] + "<br>";`
`text += cars[4] + "<br>";`
`text += cars[5] + "<br>";`
You can write:
`for (let i = 0; i < cars.length; i++) {`
`  text += cars[i] + "<br>";`
`}`

## for loop
for loop is created with 3 optional expressions
`for (expr1; expr2; expr3)`
expr1 = executed one time before the execution of code block
expr2 = defines the condition for executing the code block
expr3 = executed every time the code block has been executed

`i++` increments the i value by 1 every time the loop finishes.

`can be used to iterate through an array:`
`const cars = ["BMW", "Volvo", "Saab", "Ford"];`
`let len = cars.length;`

`let text = "";`
`for (let i = 0; i < len; i++) {`
`  text += cars[i];`
`}`

example using var:

`var i = 5;`

`for (var i = 0; i < 10; i++) {`
`  // some code`
`}`

`// Here i is 10`

using var, the variable declared in the loop redeclares the variable outside the loop

Example using let:

`let i = 5;`

`for (let i = 0; i < 10; i++) {`
`  // some code`
`}`

`// Here i is 5`

using let, the variable declared in the loop does not redeclare the variable outside the loop.

## while loop
runs block of code over and over again until condition is met

`while (i < 10) {`
`  text += "The number is " + i;`
`  i++;`
`}`

## do while loop
do while is a varient of the while loop
do while will execute the clode block once (even if condition is false at start), before checking if the condition is true. The condition is checked at the end of the loop.

`do {`
`// code block to be executed`
`}`
`while (condition);`

## break
break statement jumps out of the loop or switch. terminates the execution of the loop or a switch statement.

## continue
continue statement skips the current interation in a loop. The remaining code in the iteration is skipped and processing moves to the next iteration.

`for (let i = 1; i < 10; i++) {`
`  if (i === 3) { continue; }`
`  text += "The number is " + i + "<br>";`
`}`

This code skips the value of 3

## javascript labels
a label is an identifier followed by a colon
`labelname: statement;`

a label precedes a statement or a block of code
`labelname: {`
    statements`
`}`

## continue and labelname
you are able to use continue to jump the program to another part of the code. when continue is used and then a labelname it can run that labelname block of code.

`let text = "";

`loop1: for (let j = 1; j < 5; j++) {`
`  loop2: for (let i = 1; i < 5; i++) {`
`    if (i === 3) { continue loop1; }`
`    text += i;`
`   }`
`}`

