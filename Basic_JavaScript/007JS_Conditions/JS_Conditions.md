# Conditions

Use `if` to specify a code block to be executed, if a specified condition is true
Use `else` to specify a code block to be executed, if the same condition is false
Use `else` if to specify a new condition to test, if the first condition is false
Use `switch` to specify many alternative code blocks to be executed
Use `(? :)` (ternary) as a shorthand for if...else

## syntax for if statement

`if (condition){`
`    // code to be executed`
`}`
`else if (condition){`
`   // code to be executed`
`}`
`else {`
`    // code to be executed`
`}`

## syntax for switch statement

`switch(expression) {`
`  case x:`
`    // code block`
`    break;`
`  case y:`
`    // code block`
`    break;`
`  default:`
`    // code block`
`}`

## syntax for Ternary Operator (?:)

short hand for if ... else
`condition ? expression1 : expression2`
expression1 is the value returned if condition is true
expression2 is the value returned if condition is false

example1:
`let text = (age < 18) ? "Minor" : "Adult";`

example2:
`let isMember = true;`
`let discount = isMember ? 0.2 : 0;`

## logical operators in conditionals
x = 6 and y = 3
&& = AND --> `(x < 10 && y > 1>)` is true
|| = OR  --> `(x===5 || y === 5)` is false
!  = NOT --> `!(x === y)` is true

## Nullish Coalescing Operator (??)
the ?? operator returns the right operand when the left operand is nullish (null or undefined) otherwise it returns the left operand
example:
`let name = null;`
`let text = "missing";`
`let result = name ?? text;`

when programming values can be falsey (0, empty string, false, undefined, null, NaN)
if you need to check if variable is nullish (null or undefined by okay to be empty string or false) then you can use the nullish coalescing operator