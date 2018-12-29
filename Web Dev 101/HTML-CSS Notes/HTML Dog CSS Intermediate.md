# HTML Dog Beginner CSS Tutorial
These are my notes from assignment 2, part 3
>To fill in the gaps, read through the HTML Dog beginner HTML tutorial, the HTML Dog beginner CSS tutorial and the **HTML Dog intermediate CSS tutorial**. They should go relatively quickly since you’ve seen much of it before but you’ll find a fair bit of new information as well.
## Table of Contents

## HTML Dog Intermediate CSS Tutorial

### Class and ID selectors
* define your own selectors in the form of **class** and **ID** selectors
  * you can have the same HTML element, but show it diff depending on its class or ID!
  * class name is like **.className**
  * selector name is like **#selectorName** (ID)
```CSS
#selector {
  background-color: #ccc;
}
.class {
  color: blue;
}
```
in HTML, you refer to the CSS like so:
```HTML
<div id="selector">
  <h1>The above id assigns the element a selector</h1>
  <p class="class">The class assignment gives p a class!</p>
</div>
```
* **Difference between an ID and a Class:**
  * ID: can be used to identify **one** element
  * Class: can be used to identify **multiple** elements
* apply a selector to a specific HTML element by doing:
```CSS
p.jam{
  color:red;
}
```
* the above will only apply to **paragraph** elements with the **class jam**
---
### Grouping and Nesting
#### Grouping
* you can reduce the length of your code, giving the same properties to a number of selectors without repetition
* separate selectors/classes with a comma
```CSS
h2, .thisOtherClass, .yetAnotherClass{
  color:blue;
}
```
#### Nesting
* specify properties to selectors **within** other selectors
```CSS
#top {
    background-color: #ccc;
    padding: 1em
}

#top h1 {
    color: #ff0;
}

#top p {
    color: red;
    font-weight: bold;
}
```
* this removes need for classes or IDs on elements inside a a larger element (like div)
  * essentially says "h1 inside top should be ... and p inside top should be ..."
---
### Pseudo Classes
* added onto selectors to **specify a state or relation to the selector**
* **selector:pseudo_class{property:value;}**
#### Links
