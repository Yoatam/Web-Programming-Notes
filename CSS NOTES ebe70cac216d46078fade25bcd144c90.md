# CSS NOTES

CSS stands for Cascading Style Sheets. CSS describes how HTML elements are to be displayed on screen, paper, or in other media

CSS is used to define styles for your web pages, including the design, layout and variations in display for different devices and screen sizes.

CSS Syntax

The selector points to the HTML element you want to style.

The declaration block contains one or more declarations separated by semicolons.

Each declaration includes a CSS property name and a value, separated by a colon.

Multiple CSS declarations are separated with semicolons, and declaration blocks are surrounded by curly braces.

![img_selector.gif](CSS%20NOTES%20ebe70cac216d46078fade25bcd144c90/img_selector.gif)

```html
body {
  background-color: lightblue;
}

h1 {
  color: white;
  text-align: center;
}

p {
  font-family: verdana;
  font-size: 20px;
}
```

## CSS Id Selector

The id selector uses the id attribute of an HTML element to select a specific element. To select an element with a specific id, write a hash (#) character, followed by the id of the element.

```html
#para1 {
  text-align: center;
  color: red;
}
```

## CSS Class Selector

The class selector selects HTML elements with a specific class attribute. To select elements with a specific class, write a period (.) character, followed by the class name.

```html
.center {
  text-align: center;
  color: red;
}
```

## CSS Universal Selector

The universal selector (*) selects all HTML elements on the page.

```html
* {
  text-align: center;
  color: blue;
}
```

## CSS Grouping Selector

The grouping selector selects all the HTML elements with the same style definitions.

```html
h1 {
  text-align: center;
  color: red;
}

h2 {
  text-align: center;
  color: red;
}

p {
  text-align: center;
  color: red;
}
```

## HOW  TO ADD CSS

### 1. External CSS

With an external style sheet, you can change the look of an entire website by changing just one file. Each HTML page must include a reference to the external style sheet file inside the <link> element, inside the head section.

```html
<!DOCTYPE html>
<html>
<head>
<link rel="stylesheet" href="mystyle.css">
</head>
<body>

<h1>This is a heading</h1>
<p>This is a paragraph.</p>

</body>
</html>
```

### 2. Internal CSS

An internal style sheet may be used if one single HTML page has a unique style. The internal style is defined inside the <style> element, inside the head section.

```html
<!DOCTYPE html>
<html>
<head>
<style>
body {
  background-color: linen;
}

h1 {
  color: maroon;
  margin-left: 40px;
}
</style>
</head>
<body>

<h1>This is a heading</h1>
<p>This is a paragraph.</p>

</body>
</html>
```

### 3. Inline CSS

An inline style may be used to apply a unique style for a single element. To use inline styles, add the style attribute to the relevant element. The style attribute can contain any CSS property.

```html
<!DOCTYPE html>
<html>
<body>

<h1 style="color:blue;text-align:center;">This is a heading</h1>
<p style="color:red;">This is a paragraph.</p>

</body>
</html>
```

## CSS Margins

Margins are used to create space around elements, outside of any defined borders.

The CSS `margin` properties are used to create space around elements, outside of any defined borders. With CSS, you have full control over the margins. There are properties for setting the margin for each side of an element (top, right, bottom, and left).

CSS has properties for specifying the margin for each side of an element:

- `margin-top:` Sets the top margin of an element
- `margin-right:` Sets the right margin of an element
- `margin-bottom:` Sets the bottom margin of an element
- `margin-left:` Sets the left margin of an element

```html
p {
  margin-top: 100px;
  margin-bottom: 100px;
  margin-right: 150px;
  margin-left: 80px;
}
```

All the margin properties can have the following values:

### 1. The Auto Value

You can set the margin property to `auto` to horizontally center the element within its container.

The element will then take up the specified width, and the remaining space will be split equally between the left and right margins.

```html
div {
  width: 300px;
  margin: auto;
  border: 1px solid red;
}
```

### 2. The Inherit Value

This example lets the left margin of the <p class="ex1"> element be inherited from the parent element (<div>):

```html
div {
  border: 1px solid red;
  margin-left: 100px;
}

p.ex1 {
  margin-left: inherit;
}
```

## CSS Padding

The CSS `padding` properties are used to generate space around an element's content, inside of any defined borders.

The `padding` property is a shorthand property for the following individual padding properties:

- `padding-top:` Sets the padding to the top of an element.
- `padding-right:` Sets the padding to the right of an element.
- `padding-bottom:` Sets the padding to the bottom of an element.
- `padding-left:` Sets the padding to the left of an element.

```html
p {
  padding-top: 20px;
  padding-right: 10px;
  padding-bottom: 20px;
  padding-left: 10px;
}

```

## CSS Box Model

The CSS box model is essentially a box that wraps around every HTML element. It consists of

- **Content** - The content of the box, where text and images appear
- **Padding** - Clears an area around the content. The padding is transparent
- **Border** - A border that goes around the padding and content
- **Margin** - Clears an area outside the border. The margin is transparent

```html
div {
  width: 300px;
  border: 15px solid green;
  padding: 50px;
  margin: 20px;
}
```

## CSS Icons

To add CSS icons to your HTML page, you can use an icon library like Font Awesome. Here's an example of how to add an icon using Font Awesome:

```html
<!DOCTYPE html>
<html>
<head>
<script src="https://kit.fontawesome.com/a076d05399.js" crossorigin="anonymous"></script>
</head>
<body>

<i class="fas fa-cloud"></i>
<i class="fas fa-heart"></i>
<i class="fas fa-car"></i>
<i class="fas fa-file"></i>
<i class="fas fa-bars"></i>

</body>
</html>

```

## CSS Links

With CSS, links can be styled in many different ways

- `a:link` - a normal, unvisited link
- `a:visited` - a link the user has visited
- `a:hover` - a link when the user mouses over it
- `a:active` - a link the moment it is clicked

Also they  can be styled with any CSS property (e.g. `color`, `font-family`, `background`, etc.).

```html

a:link {color: red;
     text-decoration: none;
     background-color: yellow;
}

a:visited { color: green;
     text-decoration: none;
     background-color: blue;
}

a:hover { color: hotpink;
      text-decoration: underline;
      background-color: red;
}

a:active { color: blue;
      text-decoration: underline;
       background-color: pink;
}
```

## CSS Overflow

The CSS `overflow` property controls what happens to content that is too big to fit into an area. It specifies whether to clip the content or to add scrollbars when the content of an element is too big to fit in the specified area. 

- `visible` - Default. The overflow is not clipped. The content renders outside the element's box
- `hidden` - The overflow is clipped, and the rest of the content will be invisible
- `scroll` - The overflow is clipped, and a scrollbar is added to see the rest of the content
- `auto` - Similar to `scroll`, but it adds scrollbars only when necessary

```html
div {
  overflow: visible;
}

div {
  overflow: scroll;
}

div {
  overflow: hidden;
}

div {
  overflow: auto;
}
```

## CSS Math Functions

The CSS math functions allow mathematical expressions to be used as property values. Here, we will explain the `calc()`, `max()` and `min()` functions.

### The calc() function

The `calc()` function performs a calculation to be used as the property value.

```html
.div {
  width: calc(100% - 100px); 
}
```

### The max() and min() function

The `max()` function uses the largest value, from a comma-separated list of values, as the property value.

The `min()` function uses the smallest value, from a comma-separated list of values, as the property value.

```html
.div {
  width: max(50%, 100px); 
}
.div {
  width: min(50%, 100px); 
}
```