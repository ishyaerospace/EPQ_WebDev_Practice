# Bind() keyword.

bind() method can borrow a method from another object.
bind() method does not run the function immediately, instead it creates and returns a new function that can be called later


Bind() syntax
const NewFunction = functionname.bind(this, arg1, arg2, ...)

# bind with fix
most common way to use "this" with bind method is to have "this" set to the "this" value of the borrowed method.

`const person1 = { name: "John" };`
`const person2 = { name: "Paul" };`
`const person3 = { name: "Ringo" };`

`function greet() {`
`  return "Hello " + this.name;`
`}`

`const greetJohn = greet.bind(person1);` // greetJohn is new function that uses person1 as "this" value

`greetJohn();`


The bind method is used to preserve the value of "this"

arguaments passed to bind become fixed values, this is called partial application.
this sets the arguaments as arguments in the borrowed function.


