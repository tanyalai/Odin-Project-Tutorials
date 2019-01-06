# Numbers JavaScript Notes
These are my notes for the "Numbers" module of this assignment

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
  * so will "100" * "10", and using the - operator
  * but "100" + "10" will yield "10010"
#### NaN - Not a Number
Stuff that can yield NaN:
  * arithmetic with a non-numeric string
* use **isNan()** to find out if a value is a number
* used in a mathematical operation, result will either be NaN or a concatenation (if w/ strings)
* NaN **is** a number
#### Infinity
* returned if you can't calculate a number outside the largest possible number
* anything divided by 0 will be infinity (respective positive or negative depending on what is involved in the operation)
* it is a number
* you can store **hexadecimal** in variables
  * Js will interpret numeric constants as hexadecimal if they are **preceded by 0x**
#### Numbers Can be Objects
* you can either set them as literals like, var x = 123;
* or you can define them as objects with the keyword new like var y = new Number(123);
* **DON'T CREATE NUMBER OBJECTS THOUGH, THEY SLOW DOWN EXECUTION SPEED**
* when using == between a number and a number object of the same value, equal numbers **are indeed** equal
* but when using === for the same case described above, equal numbers are not equal because the operator expects the **same type and value**
#### Number Methods and Properties
* when using methods and properties, Js treats primitive values like objects (although, intrinsically, such primitive values can't have properties and methods)
* **toString()**  returns number as a string
* **toExponential()** returns a string, with a number rounded and written using exponential notation
```JavaScript
var x = 9.656;
x.toExponential(2);     // returns 9.66e+0
x.toExponential(4);     // returns 9.6560e+0
x.toExponential(6);     // returns 9.656000e+0
```
* **toFixed()** returns a string, with the number written with a specified number of decimals
  * ex. x.toFixed(2), where x is 3.14159, yields 3.14
* **toPrecision()** returns a string, with a number written with the specified number of sig figs
  * ex. x.toFixed(3), where x is 3.14159, yields 3.14
* **valueOf()** returns a number as a primitive value, number type
#### Converting Variables to Numbers
* **Number()**, **parseInt()**, and **parseFloat()** are **not number methods**, but are **global methods**
* **Number()** returns a number, **parseFloat()** parses argument and returns floating point number, **parseInt()** parses argument and returns an integer
  * **Number()** can work on dates, converting the date to the number of milliseconds since 1.1.1970
  * **parseInt()** allows spaces, in that case only the first number is returned
  * **parseFloat()** has similar rules to parseInt
#### Number Properties
* MAX_VALUE returns largest number possible in Js
* MIN_VALUE returns smallest number possible in Js
* POSITIVE_INFINITY represents infinity (returned when overflow)
* NEGATIVE_INFINITY represents negative infinity (returned when overflow)
* NaN discussed prior
* use these properties like Number.Property
* **Cannot be used on variables**, can only be accessed like **Number.Property**
#### Arithmetic
* ** is used for exponentiation, so 5 ** 3 is 125, or 5^3
* x++ (like Java, unlike ++x in C++)
