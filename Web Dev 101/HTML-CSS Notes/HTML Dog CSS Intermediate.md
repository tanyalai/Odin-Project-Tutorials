# HTML Dog Beginner CSS Tutorial
These are my notes from assignment 2, part 3
>To fill in the gaps, read through the HTML Dog beginner HTML tutorial, the HTML Dog beginner CSS tutorial and the **HTML Dog intermediate CSS tutorial**. They should go relatively quickly since you’ve seen much of it before but you’ll find a fair bit of new information as well.
## Table of Contents
* [Class and ID Selectors](#class-and-id-selectors)
* [Grouping and Nesting](#grouping-and-nesting)
* [Pseudo Classes](#pseudo-classes)
* [Shorthand Properties](#shorthand-properties)
## HTML Dog Intermediate CSS Tutorial

### Class and ID Selectors
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
* **selector:pseudo_class{
  property:value;
  }**
#### Links
* **link** targets unvisited links, **visited** targets visited links
```CSS
a:link{
  color:blue;
}
a:visited{
  color:purple;
}
```
* "a" is the selector for a link, link/visited are p. classes
#### Dynamic Pseudo Classes
* commonly used for links, can also apply styles when an event occurs to an item on the page
  * ex. change the style of a box when the cursor hovers over it
* **active**, when something activated by user (ex. clicked link)
* **hover**, when something is passed over by user input (ex. cursor)
* **focus**, when something is chosen or is ready for keyboard input
  * focus often found on form elements, can be used for links
#### First Children
* **first-child**, only targets the **very first descendant** of an element
ex. the following HTML:
```HTML
<body>
    <p>I’m the body’s first paragraph child. I rule. Obey me.</p>
    <p>I resent you.</p>
</body>
```
and the CSS:
```CSS
p:first-child{
  font-weight: bold;
  font-size:40px;
}
```
* this makes it so **only the first paragraph** is styled
---
### Shorthand Properties
* some CSS properties allow a string of values, separated by spaces
#### Margins and Padding
* you can just use **margin** instead of margin-top, -right, -bottom, and -left.
* use: **margin: tpx rpx bpx lpx;**
ex:
```CSS
p {
    margin: 1px 5px 10px 20px;
}
```
* can do the same with padding: top, right, bottom left.
* you can also state just **two values**, like padding: 1em 10em; or margin: 2px 10px.
* first value is **top and bottom**, second value is **right and left**
#### Borders
* use border-width in the same fashion as described above
* you can also combine the width, color, and style simply by invoking the **border property**, order doesn't matter to much
```CSS
p{
  border: 1px red solid;
}
```
* this pattern can also be applied to the border specifications (ex. -top, and -right)
#### Fonts
```CSS
p{
  font: italic bold 12px/2 courier;
}
```
* order: -style, -weight, -size, line-height, font-family
---
### Background Images
* shorthand for background:
```CSS
body {
    background: white url(http://www.htmldog.com/images/bg.gif) no-repeat top right;
}
```
* **background-color**, self-explanatory
* **background-image**, location of image
* **background-repeat**, how image repeats itself. Possible values:
  * **repeat**, equiv. of a tile effect across entire background
  * **repeat-y**, repeat on y-axis
  * **repeat-x**, repeat on x-axis
  * **no-repeat**, one instance
* **background-position**, top, center, bottom, left, right, a length, a percentage, or any **sensible** combination (etc. top right)
