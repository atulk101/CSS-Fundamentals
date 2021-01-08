# CSS-Fundamentals #

# margin:0 auto;

When you set two values on a property like margin or padding, the first value affects the element's top and bottom side (setting it to 0 in this case); the second value affects the left and right side. (Here, auto is a special value that divides the available horizontal space evenly between left and right)

# padding: 0 20px 20px 20px;

This sets four values for padding. The goal is to put  some space around the content. In this example, there is no padding on the top of the body, and 20 pixels on the right, bottom and left. The values set top, right, bottom, left, in that order.

# border: 5px solid black

This sets values for the width, style and color of the border

# text-shadow: 3px 3px 1px black;

text-shadow applies a shadow to the text content of the element. Its four values are:
The first pixel value sets the horizontal offset of the shadow from the text: how far it moves across.
The second pixel value sets the vertical offset of the shadow from the text: how far it moves down.
The third pixel value sets the blur radius of the shadow. A larger value produces a more fuzzy-looking shadow.
The fourth value sets the base color of the shadow.

# display: block; margin: 0 auto;

Makes inline element to the center of Page.

A block element can have margin and other spacing values applied to it. In contrast, images are inline elements. It is not possible to apply margin or spacing values to inline elements. So to apply margins to the image, we must give the image block-level behavior using display: block;.

# @import 'styles2.css';
@import imports a stylesheet into another CSS stylesheet

# Media Query Example

body {
  background-color: pink;
}

@media (min-width: 30em) {
  body {
    background-color: blue;
  }
}

changes styles based on the viewport width

# short hand syntax
background: red url(bg-graphic.png) 10px 10px repeat-x fixed;
is equivalent to these five lines:

background-color: red;
background-image: url(bg-graphic.png);
background-position: 10px 10px;
background-repeat: repeat-x;
background-attachment: fixed;






