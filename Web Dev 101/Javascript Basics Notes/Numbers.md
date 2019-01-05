# Numbers JavaScript Notes
These are my notes for the "Numbers" module of this assignment
## Table of Contents
* [Title](#link)

### W3Schools Lesson
* has only one type of number
  * can be with or without decimals, scientific notation or non scientific
```JavaScript
var x = 3.14;
```
#### JavaScript Numbers are Always 64-bit Floating Point
* Unlike Java or C++ with integers, short, long, etc.
* always double precision floating point numbers
#### Precision
* Integers (**numbers without a period or exponent notation**, remember they are still double floating point though) are **accurate up to 15 digits**
```JavaScript
var x = 999999999999999; //x will be <<that number
var y = 9999999999999999; //y will be 10000000000000000
```
* maximum number of decimals is 17, but floating point math is not always 100% accurate
#### Adding Numbers and Strings
* add two numbers, result is a number
* add two strings, result is a string concatenation
* add a string and a number, **result is a string concatenation**
  * ex. "10" + 20 becomes "1020"
  * so thus, a common mistake is expecting the following to be "The result is 30":
    * var z = "The result is: " + 10 + 20; but no... in actuality, what z holds is "The result is: 1020"
  * similarly the following is expected to be 102030
```JavaScript
var x = 10;
var y = 20;
var z = "30";
var result = x + y + z;
```
  * the result is actually "3030"
#### Numeric Strings
* given numeric operations, JavaScript will try to convert strings to numbers. So:
  * "100"/"10" will work (it will be 10, as in a number)
  * so will "100" * "10"
