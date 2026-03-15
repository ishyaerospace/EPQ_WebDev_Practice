# modules in JavaScript
block of code that can export and import functions and variables
Module File "math.js:
`// Export an "add" function`
`export function add(a, b) {`
`  return a + b;`
`}`
Module Script:
`<script type="module">`

`// Import the add function`
`import { add } from './math.js';`

`let result = add(2, 3);`

`</script>`

can do:
module file:
`export const variable = "value";`

module script:
`<script type="module">`
`    import {variable} from "./module.js";`
`</script>`

NOTE: module operates in strict mode.

you import named exports using {}

## default exports
this i have seen using nodejs
default export exports one main value from a module. this gives clear intent about the module's primary functionality.
only one default export can be used in a file.

## default imports
default import is the way to import the primary exported values from a module - the one that was exported using export default.

you can give default export any name during import without using curly brackets

## name space

`import * as math from "./math_module.js";` similar to python.