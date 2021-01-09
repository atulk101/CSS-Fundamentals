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

# Inheritance
some CSS property values set on parent elements are inherited by their child elements, and some aren't.

For example, if you set a color and font-family on an element, every element inside it will also be styled with that color and font, unless you've applied different color and font values directly to them

Things like widths, margins, padding, and borders do not inherit.

    => inherit
      Sets the property value applied to a selected element to be the same as that of its parent element. Effectively, this "turns on inheritance".
    => initial
      Sets the property value applied to a selected element to the initial value of that property.
    => unset
      Resets the property to its natural value, which means that if the property is naturally inherited it acts like inherit, otherwise it acts like initial.

# all:unset
sets the value of all to unset

# background vs background color

With background you can set all background properties like:

background-color
background-image
background-repeat
background-position
etc.
With background-color you can just specify the color of the background

# text-decoration: none

Can be used for removing text style from link

# list-style-type: none

Remove list style 

# !important
This is used to make a particular property and value the most specific thing, thus overriding the normal rules of the cascade.

# Type, class, and ID selectors

This group includes selectors that target an HTML element such as an <h1>.

h1 { }

It also includes selectors which target a class:

.box { }
or, an ID:

#unique { }

# Attribute selectors

This group of selectors gives you different ways to select elements based on the presence of a certain attribute on an element:

a[title] { }

Or even make a selection based on the presence of an attribute with a particular value:

a[href="https://example.com"] { }

# Pseudo-classes and pseudo-elements

This group of selectors includes pseudo-classes, which style certain states of an element. The :hover pseudo-class for example selects an element only when it is being hovered over by the mouse pointer:

a:hover { }

It also includes pseudo-elements, which select a certain part of an element rather than the element itself. For example, ::first-line always selects the first line of text inside an element.

p::first-line { }

# Combinators
The final group of selectors combine other selectors in order to target elements within our documents. The following for example selects paragraphs that are direct children of <article> elements using the child combinator (>):

article > p { }

# Universal Selector (*)
  * {
      margin: 0;
  }
selects everything in document.

# Attribute presence and value selectors

By using li[class] we can match any selector with a class attribute. This matches all of the list items except the first one.
li[class="a"] matches a selector with a class of a, but not a selector with a class of a with another space-separated class as part of the value. It selects the second list item.
li[class~="a"] will match a class of a but also a value that contains the class of a as part of a whitespace-separated list. It selects the second and third list items.

# Substring matching selectors
li[class^="a"] matches any attribute value which starts with a, so matches the first two list items.
li[class$="a"] matches any attribute value that ends with a, so matches the first and third list item.
li[class*="a"] matches any attribute value where a appears anywhere in the string, so it matches all of our list items.

# Case-sensitivity
If you want to match attribute values case-insensitively you can use the value i before the closing bracket.
Example-
li[class^="a" i] {
    color: red;
}

# Pseudo-class?

A pseudo-class is a selector that selects elements that are in a specific state, e.g. they are the first element of their type, or they are being hovered over by the mouse pointer. They tend to act as if you had applied a class to some part of your document
  Pseudo-classes are keywords that start with a colon:
  :pseudo-class-name  
  example:
    :first-child
    :last-child
    :only-child
    :only-of-type
    :invalid

# :last-child

The :last-child CSS pseudo-class represents the last element among a group of sibling elements.
  /* Selects any <p> that is the last element among its siblings */
  p:last-child {
    color: lime;
  }
# :only-child

The :only-child CSS pseudo-class represents an element without any siblings. This is the same as :first-child:last-child or :nth-child(1):nth-last-child(1), but with a lower specificity
  /* Selects each <p>, but only if it is the */
  /* only child of its parent */
  p:only-child {
    background-color: lime;
  }

# :invalid

The :invalid CSS pseudo-class represents any <input> or other <form> element whose contents fail to validate.
  /* Selects any invalid <input> */
  input:invalid {
    background-color: pink;
  } 

# :only-of-type 

The :only-of-type CSS pseudo-class represents an element that has no siblings of the same type.

# :User-action pseudo classes






