# JS Function call()
The JS call() method can be used to call a function with a specific "this"
the call() method lets an object use a method belonging to another object

this allows same method to be used on different objects

call syntax:
`functionName.call(this, arg1, arg2, ...);`
replace "this" with the object 

example:
`const person1 = { name: "John" };`
`const person2 = { name: "Paul" };`
`const person3 = { name: "Ringo" };`

`function greet(greeting) {`
`  return greeting + " " + this.name;`
`}`

`greet.call(person3, "Hello");`

