# HTML and CSS Basics Notes from HTML Dog
These are my notes from assignment 2
>To fill in the gaps, read through the HTML Dog beginner HTML tutorial, the HTML Dog beginner CSS tutorial and the HTML Dog intermediate CSS tutorial. They should go relatively quickly since you’ve seen much of it before but you’ll find a fair bit of new information as well.
## Table of Contents
* [HTML Dog Beginner HTML Tutorial](#html-dog-beginner-html-tutorial)
  * [Tags, Attributes, and Elements](#tags-attributes-and-elements)
  * [Page Titles](#page-titles)
  * [Paragraphs](#paragraphs)
  * [Headings](#headings)
  * [Lists](#lists)
  * [Links](#links)
  * [Images](#images)
* [HTML Dog Beginner CSS Tutorial](#html-dog-beginner-css-tutorial)
* [HTML Dog Intermediate CSS Tutorial](#html-dog-intermediate-css-tutorial)
## HTML Dog Beginner HTML Tutorial
Remember to include **.html** at the end of HTML files.
### Tags, Attributes, and Elements
#### Tags
* basic structure that surrounds content and gives meaning (not presentation)
```HTML
<!DOCTYPE html>
<html>
<body>
  This is my first web page
</body>
</html>
```
* \<!DOCTYPE html\> is a **document type declaration**
* lets browser know the type of HTML used
* ex. \<html\> is opening, **</** html> is closing
  * but not all tags have closing like ^^. Some that don't wrap around content will close themselves
  * ex. \<br\> , which is a line break.
* **Closing Rule:** Content between? </..>
#### Attributes
* extra bits of information that give a "flavor" to the HTML
```HTML
<tag attribute = "value"> Margarine </tag>
```
#### Elements
* component that makes up web pages.
* ex. stuff in between \<body\> tags are part of body element
---
### Page Titles
```HTML
<head>
  <title>My first web page</title>
</head>
```
* The information in the head element **doesn't** appear in the browser
* Instead, it appears on a tab or the title bar of the window!
---
### Paragraphs
* p tag is used for paragraphs
```html
<p>Example paragraph with proper HTML5 syntax</p>
```
#### Emphasis
* emphasize text **inside** paragraph using **em** (emphasis) and **strong** (strong importance)
```HTML
<p>Example <em>paragraph</em> with <strong>proper</strong> syntax</p>
```
* **em** often shows in *italics*
* **strong** often in **bold**
* the above are not the same as **i** and **b** tags
#### Line breaks
* mentioned prior. Just \<br\>. No closing tag.
* don't use if two blocks of text are needed to be separate from each other. Just use \<p\>
---
### Headings
* six levels of heading tags, strongest to least strong: h1, h2, h3, h4, h5, h6.
* best practice to use the h1 tag only once, signifying the main heading of the page.
---
### Lists
* three types of lists: unordered, ordered, definition (discussed later)
* sequential use ordered, preceded by numbers
* non-sequential use unordered, preceded by actual bullets
* **ol** for ordered lists, **ul** for unordered lists
* **li** for each list item
* you can put lists inside other lists!
---
### Links
* HT in HTML stand for hypertext, a system of linked hypertext
* **a** is an *anchor* tag, used to define link. In addition to this, the destination of link must be added
```HTML
<p><a href="http://www.htmldog.com">HTML Dog</a></p>
```
* destination defined in **href** attribute. It can either be absolute or relative
* ex. to link to another file in the same directory, it could be \<a href="other.html"\>Other HTML\</a\>
* to send a user to another part of the same page they are on, use an **id** attribute to any tag
```HTML
<h2 id="about">About Me</h2>
<!-- The above is the set up. Then link to that section by: -->
<a href="#about">Go to About Me</a>
```
---
### Images
```HTML5
<img src="http://www.htmldog.com/badgel.gif" width="120" height="90" alt="HTML Dog">
```
* **src** tells browser where to find the image. Can either be absolute or relative (ex. src="images/image.jpg")
* **width** and **height** self explanatory. Necessary or else the browser will calculate image size as it loads, leading to *jank* images.
* **alt** is the alternative description
* **JPEG** typically used for photographs, **GIFS** used for solid colors (ex. icons, logos) or small animations, **PNG** versatile images w/ more complex designs (note: not fully supported by older browsers)
---
### Tables
* **table** defines the table, **tr** defines table row, **td** defines a data cell.
```HTML5
<table>
  <tr>
    <td>Apple</td>
    <td>Orange</td>
  </tr>
  <tr>
    <td>Pear</td>
    <td>Grape</td>
  </tr>
</table>
```
---
### Forms




## HTML Dog Beginner CSS Tutorial

## HTML Dog Intermediate CSS Tutorial
