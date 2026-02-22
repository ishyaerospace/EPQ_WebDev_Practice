# Arrays
JS arrays are dynamic in size and therefore support methods that can add or remove elements from the array. --> changes size of array

JS arrays can also store different data types within the same array.

syntax
`const array_name = [item1, item2, ...];`

you can create an empty array and add elements after

`const cars = [];`
`cars[0]= "Saab";`
`cars[1]= "Volvo";`
`cars[2]= "BMW";`

no need to use "new Array()"

## converting an array to strings

.toString(); gives a comma sepeated string of values

`const fruits = ["Banana", "Orange", "Apple", "Mango"];`
`document.getElementById("demo").innerHTML = fruits.toString();`

## access full array

the full array can be accessed by referring to the arry name:

`const cars = ["Saab", "Volvo", "BMW"];`
`document.getElementById("demo").innerHTML = cars;`

.push(value) adds a new lement to the array

however adding elements with high indexes that are greater than the (length of the array + 1) can create undefines "holes" in the array

also if you use named indexes rather than numbered indexes to assign value to the array then the array will become an object and the array methods and properties will produce inccorect results.

typeOf array; will give "object" as JS array acts as objects
array.isArray(array); will return if the array is an array