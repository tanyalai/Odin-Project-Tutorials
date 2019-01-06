#Variables Notes
## JavaScript.Info Lesson
### Variables
* named storage for data
* create variable using the *let* keyword
```JavaScript
let message = 'Hello'; // store the string
```
* declare multiple variables in one line by separating each declaration with a comma
* you can also declare using the *var* keyword, it's almost the same but it's mostly just old-school
### Variable Naming
* name must only contain letters, digits, symbols $ and _
* the first character must not be a digit
* cannot be a reserved word, some include: let, class, return, function
* the following is bad practice because it won't work when "use strict"; is declare before the following chunk of code:
```JavaScript
// note: no "use strict" in this example
num = 5; // the variable "num" is created if didn't exist
alert(num); // 5
```
* declare a constant, unchanging var by using the *const* keyword instead of let or var
* uppercase names for **HARD-CODED VALUES** (constants where the value never changes, both before and after the program is run) and underscores for spaces (common practice)
