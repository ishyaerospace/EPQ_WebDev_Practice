# Function closure.

global variables can be made local (private).
function remembers the variables from its outer scope, even after function finishes running.

if variable is initialised outside of the function any function can access the variable and change its value.
if the variable is initialised inside function, every time it is called the variable will be reset.
if a nested function is used to access a variable within its parent class, it could work if the varaible only ran once.

## nested functions with closure
`function myCounter() {`
`  let counter = 0;`
`  return function() {`
`    counter++;`
`    return counter;`
`  };`
`}`
`const add = myCounter();`
`add();`
`add();`
`add();`

`// the counter is now 3`

the add variable is assigned to the return value of the function, the function only runs once. it sets the value to 0, and returns a function expression. This is a closure

closure:
* creates private variables
* preserve state between function calls
* simulates block-scoping before let and const existed
* implements certain design patterns like currying and memorisation.

# moden ALTERNATIVE
since 2022 JS has added pure private variables, therefore closure method of making variables private is no longer needed as it is harder to implement.

JS uses the `#` syntax to create private class fields.

`class Counter {`
`  #count = 0;`

`  increment() {`
`    this.#count++;`
`    return this.#count;`
`  }`
`}`

`const myCounter = new Counter();`
`myCounter.increment();`
