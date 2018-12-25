# HTML and CSS Basics Notes from HTML Dog
These are my notes from assignment 2
>To fill in the gaps, read through the HTML Dog beginner HTML tutorial, the HTML Dog beginner CSS tutorial and the HTML Dog intermediate CSS tutorial. They should go relatively quickly since you’ve seen much of it before but you’ll find a fair bit of new information as well.
## Table of Contents
* [HTML Dog Beginner HTML Tutorial](#html-dog-beginner-html-tutorial)
  * [Tags, Attributes, and Elements](#tags-,-attributes-,-and-elements)
  * [Page Titles](#page-titles)
  * [Paragraphs](#paragraphs)
  * [Headings](#headings)
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


## HTML Dog Beginner CSS Tutorial

## HTML Dog Intermediate CSS Tutorial
