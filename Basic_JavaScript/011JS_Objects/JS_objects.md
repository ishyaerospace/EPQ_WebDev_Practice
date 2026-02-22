# objects

`// Create an Object`
`const person = {`
`  firstName: "John",`
`  lastName: "Doe",`
`  age: 50,`
`  eyeColor: "blue"`
`};`

you can also create an empty object and then add properties after

`// Create an Object`
`const person = {};`

`// Add Properties`
`person.firstName = "John";`
`person.lastName = "Doe";`
`person.age = 50;`
`person.eyeColor = "blue";`

no need to use ""new Object()"

## acccessing properties
dot notation: objectName.propertyName;
bracket Notation: objectName["propertyName"];

## this

in an object method, "this" refers to the object

`const person = {`
`  firstName: "John",`
`  lastName : "Doe",`
`  age      : 50,`
`  fullName : function() {`
`    return this.firstName + " " + this.lastName;`
`  }`
`};`

## delete properties
delete keyword deleted both the value and the property
after deleting, the property is removed. accessing it will return "undefined"

`const person = {`
`  firstName: "John",`
`  lastName: "Doe",`
`  age: 50,`
`};`

`delete person["age"]; // delete person.age;`

## in operator

in is used to check if a property still exists in an object

`const person = {`
`  firstName: "John",`
`  lastName: "Doe"`
`};`

`let result = ("firstName" in person);`


## methods
`objectName.methodName();`

if called without brackets it will return the function definition:
`objectName.methodName;`

you can assign functions to properties to add methods to objects.

`// Assign person.name to a function`
`person.name = function () {`
`  return this.firstName + " " + this.lastName;`
`};`

## object constructors

sometimes many objects with the same type needs to be made. to create an object type we use an object constructor function. It is considered good practice to name constructor functions with an upper-case first letter.

`function Person(first, last, age, eye) {`
`  this.firstName = first;`
`  this.lastName = last;`
`  this.age = age;`
`  this.eyeColor = eye;`
`}`

now the "new Object" can be used to create multiple objects
`const myFather = new Person("John", "Doe", 50, "blue");`
`const myMother = new Person("Sally", "Rally", 48, "green");`
`const mySister = new Person("Anna", "Rally", 18, "green");`