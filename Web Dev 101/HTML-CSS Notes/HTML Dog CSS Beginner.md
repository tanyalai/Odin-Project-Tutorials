# HTML Dog Beginner CSS Tutorial
These are my notes from assignment 2, part 2
>To fill in the gaps, read through the HTML Dog beginner HTML tutorial, **the HTML Dog beginner CSS tutorial** and the HTML Dog intermediate CSS tutorial. They should go relatively quickly since you’ve seen much of it before but you’ll find a fair bit of new information as well.
## Table of Contents
* [Applying CSS](#applying-css)
* [Selectors, Properties, and Values](#selectors-properties-and-values)
* [Colors](#colors)
* [Text](#text)
* [Margins and Padding](#margins-and-padding)
* [Borders](#borders)
## HTML Dog Beginner CSS Tutorial
* Cascading Styles Sheet, presentation
### Applying CSS
* Three ways to apply CSS to HTML: inline, internal, and external
#### Inline
* placed directly into HTML tags using style attribute
```HTML
<p style="color: red">the text will be red</p>
```
* This is not good practice. Avoid wherever possible.
  * best practice is that HTML should be a **stand-alone, presentation free** document
#### Internal
* embedded. Inside the head element, style tag surrounds styles for whole page (still inside HTML document)
```HTML
<head>
<title>CSS Example</title>
<style>

    p {
        color: red;
    }

    a {
        color: blue;
    }

</style>
...
</head>
```
* this still isn't the best practice because HTML doc is not presentation free...
#### External
* store in a separate CSS file.
* save with **.css** in the **same directory** as the HTML page
* link CSS to HTML like this:
```HTML
<head>
  ...
  <link rel="stylesheet" href="nameofsheet.css">
  ...
</head>
```
---
### Selectors, Properties, and Values
* HTML has tags, CSS has selectors
* selectors are the *names* given to diff. styles in both internal and external style sheets
  * in this tutorial, we'll focus on HTML selectors (just the names of HTML tags)
* each selector has **properties** inside **curly brackets** (ex. {})
* value is given to the property following a **colon**
```CSS
body {
    font-size: 14px;
    color: navy;
}
```
* units: px is pixel, em is unit for calculated size of font, so ex. 2em is two times the current size, pt is points.
* when value is 0, no unit is needed.
---
### Colors
* 16,777,216 colors available (can either be by name, RGB, or hex code)
* RGB is from 0 to 255. Can also be a percentage
* Hexadecimal is a base-16 numbering system. We generally use base-10, but hexadecimal is involved in hex code.
* For hex code colors, include **#** and then either three or six characters after. ex. **#f00** is **ff0000** and **#cc9966** is **#c96**.
#### color and background-color
* foreground is color.
```css
h1 {
    color: yellow;
    background-color: blue;
}
```
---
### Text
#### font-family
* User's browser must be able to find the font you specify. It must be on their computer, or accessible via the web (ex. google fonts) otherwise
* safe fonts include Arial, Verdana, and Times New Roman
* can specify more than one font, separated by commas, as fallbacks if the user doesn't have the first specified font
```CSS
h1 {
font-family: arial, helvetica, serif;
}
```
* ex. last resort can be serif (like times) or sans-serif (more modern)
#### font-size
* self explanatory
#### font-weight
* specifies if it is bold or not.
* common is font-weight:bold or font-weight:normal
* other values are bolder, lighter, 100 - 900.
* 400 is normal, 700 is bold
#### font-style
* italic vs. normal
#### text-decoration
* underline, overline, line-through (a strike-through), none
#### text-transform
* size of text: capitalize, uppercase, lowercase, none
#### Text spacing
* **letter-spacing** and **word-spacing** properties. Can either be a length or normal. Default spacing is 0.25em.
* **line-height** sets the height of line without changing font size
* Can be a number (specifying multiple of the font size), a length, a percentage, or normal
* **text-align**: center, right, left, or justify
* **text-indent** indents the first line of a paragraph to a given length or percentage. RARELY used in digital media (web)
* you can link fonts from different websites, ex in the HTML file:
```HTML
<head>
  <link href="link from the fonts google" type="text/css" rel="stylesheet">
</head>
```
---
### Margins and Padding
* margin is the space **outside** something, padding is **inside**
* there is a -top, -right, -bottom, -left for both margin and padding.
#### The Box Model
![the box model](https://internetingishard.com/html-and-css/css-box-model/css-box-model-73a525.png)
---
### Borders
* part of the box model. Can be applied to most HTML elements within the body
* **border-style**, possible values: **solid**, **dotted**, **dashed**, **double**, **groove**, **ridge**, **inset**, and **outset**
* **border-width** sets the width of the border, using pixel value.
  * additional properties for **border-top-width**, **border-right-width**, **border-bottom-width**, and **border-left-width**
* **border-color**, self-explanatory
