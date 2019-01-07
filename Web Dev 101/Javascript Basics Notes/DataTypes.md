# Data Types
* variables in javascript can at one moment be a string and then later hold a numeric value
  * this is similar to MATLAB–**dynamic typing**!
* Seven basic data types in Js
### Number
* serves both integers and floating point numbers
* Infinity, -Infinity, and NaN belong to this type
* Infinity results as a division by zero
  * **side note:** use **alert(x)**, with what you want to show in x, to display things to an alert window!
* NaN is a computational error, resulting from an incorrect or undefined mathematical operation
### String
* can either use **""**, **''**, or **``**
* double and single quotes are simple quotes, they are EQUIVALENT
* backticks are extended functionality quotes, they allow one to embed variables and expressions into a string by wrapping with **${...}**
  * the stuff inside ${...} is evaluated and becomes part of the string, so the following works like so:
```JavaScript
let name = "John";
// embed a variable
alert( `Hello, ${name}!` ); // Hello, John!
// embed an expression
alert( `the result is ${1 + 2}` ); // the result is 3
```
### Boolean (logical type)
* two values, true and false
### Null
* **NOT** a reference to a non-existing object or a null pointer like some other languages
* it has the sense of "nothing", "empty", or "value unknown"
### Undefined
* means that value is not assigned
* ex. if value is declared but not assigned, it's value is undefined
### Objects and Symbols
* objects are **NOT** primitive, they can store collections of data and more complex things
* symbols are unique identifiers for objects (will study later)
### typeof Operator
* returns the type of the argument
* two forms of syntax: typeof x **OR** typeof(x), it will work with or without parentheses
* typeof null will return "object" and that is wrong, an error in the language
