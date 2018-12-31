# HTML Dog Beginner CSS Tutorial
These are my notes from assignment 2, part 3
>To fill in the gaps, read through the HTML Dog beginner HTML tutorial, the HTML Dog beginner CSS tutorial and the **HTML Dog intermediate CSS tutorial**. They should go relatively quickly since you’ve seen much of it before but you’ll find a fair bit of new information as well.
## Table of Contents
* [Class and ID Selectors](#class-and-id-selectors)
* [Grouping and Nesting](#grouping-and-nesting)
* [Pseudo Classes](#pseudo-classes)
* [Shorthand Properties](#shorthand-properties)
* [Background Images](#background-images)
* [Specificity](#specificity)
* [Display](#display)
* [Pseudo Elements](#pseudo-elements)
* [Page Layout](#page-layout)
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
---
### Specificity
* two or more conflicting CSS rules on same element? The more **specific** one wins
* if same specificity, the **last** one will take precedence
* but that isn't often the case. Conflicts are more common amongst **nested selectors**
* **the more specific a selector, the more preference it will be given** when it comes to conflicting styles
#### Calculating Specificity
* give every **ID selector (#selector)** a value of **100**, **class selector (.class)** a value of 10, and every **HTML selector** a value of 1
  * ex. div p has specificity value of 2 (2 HTML selectors)
---
### Display
* visual representation of most HTML elements are essentially display types
* most fundamental types: inline, block, none
* manipulated with the **display** property, with the values stated above
#### Inline
* follows the flow of a line (ex. anchor links and emphasis are inline)
```CSS
li{ display:inline; }
```
#### Block
* makes a box standalone, fitting the entire width of the containing box with a line break before and after the main element
* display: inline-block will make box inline but give formatting flexibility of the block
#### None
* can "turn off" the display of elements in certain situation
* display:none and visibility; hidden aren't the same
  * display:none takes the elements box completely out of play
  * visibility: hidden keeps the box in place without visually representing the contents
#### Tables
* can mimic tr and td elements w/ table-row, and table-cell property values (CSS)
* display offers a table-column, -row-group, column-group, -header-group, -footer-group, and -caption values
* inline-table sets table without line breaks before and after
#### Other Display Types
* **run-in** makes a box either in-line or block (depends on the parent display)
* **list-item** shows the box in the way an **li** element is expected to be displayed
  * should be nested within an **ul** or **ol** element for this to work
---
### Pseudo Elements
* stick to pseudo classes, takes form of:
```CSS
selector: pseudoelement{
  property: value;
}
```
#### First Letters and First Lines
* **first-letter** self explanatory
* **first-line** to top-most displayed line in a box
so ex.
```CSS
p:first-line{
  font-weight: bold;
}
p:first-letter{
  font-size: 30px;
}
```
* **NOTE**, CSS3 specs suggest p::first-line (with 2 colons) to differentiate them from pseudo classes. Backwards compatibility will be valid either way
#### Before and After Content
* **before** and **after** are used in conjunction with the **content** property to place content on **either side** of a box w/out touching HTML
  * use this sparingly
* values of **content** property: **open-quote**, **close-quote**, any string in quotation marks, or any image (using **url(imagename)**)
* **content** effectively creates another box to work with
```CSS
blockquote:before {
    content: open-quote;
}

blockquote:after {
    content: close-quote;
}

li:before {
    content: "POW! ";
}

p:before {
    content: url(images/jam.jpg);
}
```
---
### Page Layout
* take chunks and place them **absolutely** or **relative** to another chunk
#### Positioning
* **position** property defines the relation of the box
  * **static** is the default value. Renders in normal order, as apparent by HTML
  * **relative** is similar to static but can be offset by top, right, bottom, and left
  * **absolute** pulls box out of normal flow. Can be placed anywhere on the page, regardless, and follow top, right, bottom, and left instructions
  * **fixed** is like absolute, but will make the box position fixed in reference to the browser window, so the box stays in the exact place on screen, even when page is scrolled
    * so fixed can be kind of like a menu bar that always stays at the top of the screen with you, even as you scroll
  * downside to absolutely positioned boxes: because they live in a world of their own, can't accurately determine end location. Safer bet is to **float** the chunks, rather than absolutely positioning
#### Floating
* floating something will shift it to the **right** or **left** of a line, surrounding content flows around it
* **float:left** or **float:right**
* then, if you don't want the next box to wrap, apply the clear property, specify:
  * **clear:left**, **clear:right**, or **clear:both**
