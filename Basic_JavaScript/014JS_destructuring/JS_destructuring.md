# Destructuring in JavaScript

Destructuring Assignment Syntax:
the destructuring assignment syntax can unpack objects into variables
`let {firstName, lastName} = person;`

## structure of the destructuring in JavaScript
`// Create an Object`
`const person = {`
`  firstName: "John",`
`  lastName: "Doe",`
`  age: 50`
`};`

`// Destructuring`
`let {firstName, lastName} = person;`

The order does not matter, so the last line in the code can be:
`let {lastName, firstName} = person;`

destructuring does not change the original object.

## default object values

for missing properties you can add default values:
`let {firstName, lastName, country = "US"} = person;`


## aliasing 

you can use aliasing to set a different name to the destructured variable which can be used anywhere in the proram. 
see Aliasing.html


## strings
`// Create a String`
`let name = "W3Schools";`

`// Destructuring`
`let [a1, a2, a3, a4, a5] = name;`