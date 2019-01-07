# Strings Notes
```JavaScript
var string = 'The revolution will not be televised.';
string;
```
* you can just do string; and it will print out to the console!
* both single and double quotes will work, but don't mix them
  * strings in single or double quotes are string literals
* **\** is the escape character, so if you want to type an abbreviation like I've but you need it in 'I've' single quotes, do 'I\'ve', with the escape character before
* concatenate strings using the plus (+) operator
  * you can concatenate a mix of variables and actual strings
```JavaScript
var button = document.querySelector('button');
button.onclick = function() {
  var name = prompt('What is your name?');
  alert('Hello ' + name + ', nice to see you!');
}
```
* when this script is hooked up to a button, it uses the window.prompt() to ask the user to answer a question via a popup dialog box and stores the user input in the name variable
* Number(string) converts the string to a number type
* myNum.toString() convert a number to a string
### Useful String Methods
[Exhaustive List of String Methods](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)
* **string.length**, length of string
* Javascript is zero-indexing, get a certain character by stringName[x], last character by stringName[stringName.length-1]
* **string.indexOf(x)** finds the first index of the first occurrence of the substring
  * similarly you can use **string.lastIndexOf(x)** to find the last occurrence of a certain substring
  * -1 is returned when the substring is not found
* **string.slice(start Index, one after last Index)** to extract a substring
  * or the argument for .slice can just be one value, representing you want to extract all remaining characters from that point onwards
  * if the parameter is negative, the position is counted from the end of the string
``` JavaScript
var str = "Apple, Banana, Kiwi";
var res = str.slice(-12, -6); //res = Banana
```
* **.substring()** is similar to slice, but it can't take negative indexes
* **.substr()** is also similar to slice, but the second parameter specifies the **length** of the extracted part
```JavaScript
var str = "Apple, Banana, Kiwi";
var res = str.substr(7, 6); //res = Banana
```
* **.toLowerCase()** and **.toUppercase** respectively
* **string.replace(what you want to replace, what to replace with)** so you basically replace the **first occurrence** of the first argument with the second
  * to properly update the value, you have to do string = string.replace(x, y);
  * replace is case sensitive. To replace it with case **insensitive** use a **regular expression**, which is specified with an **/i** flag
  ```JavaScript
  str = "Please visit Microsoft!";
  var n = str.replace(/MICROSOFT/i, "W3Schools"); //this still results in a correct replacement
  ```
  * to **replace all matches**, use a regular expression with a **/g** flag (global match)
  ```JavaScript
  str = "Please visit Microsoft and Microsoft!";
  var n = str.replace(/Microsoft/g, "W3Schools");
  ```
* **.search(x)** is equivalent to indexOf in terms of what they return but they are slightly different
  * search CANNOT take a second start position argument
  * indexOf cannot take powerful search values (regular expressions?)
* **.concat(x,y)** or **str.concat(x)** joins two or more strings (concatenation), same as + operator
* **string.trim()** removes white space from both sides of a string
* **.charAt(x)** returns character at specified index
  * similar to [], but [] is more unpredictable:    
  * it doesn't work in IE7 or earlier
  * makes strings looks like arrays when they aren't
  * when no character is found, returns undefined vs. charAt() returns an empty string
  * read-only, can't say str[0]="A" to rewrite something
* **.charCodeAt(x)** returns the **unicode character** at a specified index
* convert string to array with the **.split(x)** method
  * **x** argument is telling the method what to split on, like on a comma, a space, or another character
    * if separator omitted, returned array has the whole string in the first position
    * if "" separator, the returned array will be an array of characters
