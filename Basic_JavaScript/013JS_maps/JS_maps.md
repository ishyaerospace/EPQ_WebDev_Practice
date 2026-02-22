# maps
JS maps is an object that can store collections of key-value pairs, similar to a dictionary in other languages like python. Maps differ from standard objects in that Keys can be of any data type.

* key types
    map keys can be any type
* insertion order
    map remembers the original insertion order of the keys
* size
    the number of items in a Map is easily retrieved using the size property
* performance 
    Maps are optimised for frequent additions and removeals of key-value pairs
* iteration
    maps are iterable, allowing for direct use of for...of loops or methods like forEach()
* iteration order
    the original order is preserved during iteration

maps are similar to both objects (unique key/value collections) and Arrays ( ordered vakue collection)    

create a new Map and add elements with Map.set()

`// Create an empty Map`
`const fruits = new Map();`

`// Set Map Values`
`fruits.set("apples", 500);`
`fruits.set("bananas", 300);`
`fruits.set("oranges", 200);`

you can also pass an array into the new Map() constructor

`// Create a Map`
`const fruits = new Map([`
`  ["apples", 500],`
`  ["bananas", 300],`
`  ["oranges", 200]`
`]);`

set() can also be used to change existing map values buy assigning a new value to the key

.get("key") can be used to return the value assigned to that key

Map.size() returns the number of elements in a map

Map.delete("key"); removes the map element.

Map.clear(); removes all elements from a map

Map.has("key"); returns true if the key exists in the map

## object as keys

`// Create Objects`
`const apples = {name: 'Apples'};`
`const bananas = {name: 'Bananas'};`
`const oranges = {name: 'Oranges'};`

`// Create a Map`
`const fruits = new Map();`

`// Add new Elements to the Map`
`fruits.set(apples, 500);`
`fruits.set(bananas, 300);`
`fruits.set(oranges, 200);`

the key is an object rather than a string. so `fruits.get("apples");` Returns undefined 