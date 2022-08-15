# Class 08

## Learn CSS - Flexbox

1. Flexbox is designed for one-dimensional content. Explain what this means.  
In most cases, flexbox aligns content along just one axis, either horizontal or vertical. It *can* work well for mocking up 2D content, but it was originally designed with being really good at laying things out on a single axis.
2. Explain the difference between the main axis and cross axis.  
The main axis is the axis defined by the `flex-direction` property. The cross axis is perpendicular to the main axis. `flex-direction` can be defined as row, column, row-reverse, or horizontal-reverse.
3. How can using certain properties of flexbox negatively impact accessibility?  
Reversing the order of items using one of the -reverse values in `flex-direction` *only* affects the visual order of the page, not the logical order. If `flex-direction` is used to reverse the elements and that is the expected reading order for the user, it should be kept in mind that this is not the order that screen readers will use.

## CSS Layout - Flexbox

1. What are some advantages of using flexbox over float?  
Flexbox is designed with available space and the relationship between child elements in mind. Historically, properties like `position` and `float` were used to place things on a page, but they deal mainly with absolute values. This makes centering elements and creating equal spacing very difficult, since those are inherently dynamic and determined by surrounding space.
2. How does this topic connect with your long term goals?  
Flexbox is a *very* powerful tool, and there's always a new trick to learn when using it. I may not want to be a web *designer*, but being able to neatly place elements on a page is still an important skill, even if its just for building a nice portfolio.