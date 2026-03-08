# JS "this" keyword

the "this" keyword is used in a function, it refers to an object. which object is not decided when the function is written, the value of "this" is decided when the function is called.

## "this" in an object method
when a function is an object method:
"this" referes to the object that owns the method.

`const person = {`
`  firstName: "John",`
`  lastName: "Doe",`
`  fullName: function() {`
`    return this.firstName + " " + this.lastName;`
`  }`
`};`

`person.fullName();`

"this" referes to the person object. 
this.firstName is the same as person.firstName

## GlobalThis
javascript GlobalThis is a special built-in object that provides a standard way to access the global object, regardless of the environment you code runs in (browser, node.js, web worked, or other JS runtimes)

the global object is the top-level object in JS environment
browser - window
node.js - global
web worked - it self.

## "this" in event handlers
`<button onclick="this.innerHTML='Clicked!'">Click Me</button>`
