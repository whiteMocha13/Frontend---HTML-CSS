BOX MODEL

We’ve familiarized ourselves with HTML and CSS; we know what they look like and how to accomplish some of the basics. Now we’re going to go a bit deeper and look at exactly how elements are displayed on a page and how they are sized.

How Are Elements Displayed?

Before jumping into the box model, it helps to understand how elements are displayed. To quickly recap, block-level elements occupy any available width, regardless of their content, and begin on a new line. Inline-level elements occupy only the width their content requires and line up on the same line, one after the other. Block-level elements are generally used for larger pieces of content, such as headings and structural elements. Inline-level elements are generally used for smaller pieces of content, such as a few words selected to be bold or italicized.

--------------------------------------------------------------------------------------------------------------
DISPLAY

Exactly how elements are displayed—as block-level elements, inline elements, or something else—is determined by the display property. Every element has a default display property value; however, as with all other property values, that value may be overwritten. There are quite a few values for the display property, but the most common are block, inline, inline-block, and none.

We can change an element’s display property value by selecting that element within CSS and declaring a new display property value. A value of block will make that element a block-level element.
___________________________
p {
  display: block;
}
___________________________

              
A value of inline will make that element an inline-level element.
___________________________
p {
  display: inline;
}
___________________________

              
Things get interesting with the inline-block value. Using this value will allow an element to behave as a block-level element, accepting all box model properties (which we’ll cover soon). However, the element will be displayed in line with other elements, and it will not begin on a new line by default.
___________________________
p {
  display: inline-block;
}
___________________________
              
---------------------------------------
The Space Between Inline-Block Elements
One important distinction with inline-block elements is that they are not always touching, or displayed directly against one another. Usually a small space will exist between two inline-block elements. This space, though perhaps annoying, is normal. We’ll discuss why this space exists and how to remove it in the next lesson.
---

Lastly, using a value of none will completely hide an element and render the page as if that element doesn’t exist. Any elements nested within this element will also be hidden.
________________
div {
  display: none;
}
________________


---

WHAT IS BOX MODEL? 

