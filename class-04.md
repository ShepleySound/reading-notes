# Class 04

These topics introduce HTML links, flow and positional styling in CSS, and JavaScript functions.

## Learn HTML

### Creating Hyperlinks

1. To create a basic link, we wrap text or other content inside what element?  
The `<a>` element creates a basic link.
2. The `href` attribute contains what information?  
It contains the reference to where the link should go. This can be relative, such as moving between files and directories on a web server or local machine using the *current* file's location for context, or absolute, which provides a location that remains the same regardless of where the current file is located.
3. What are some ways we can ensure links on our pages are accessible to all readers?  
All text that is important to the context of the link should be included between the opening and closing tags of the `<a>` element. Avoiding using the URL in the link text is also important, as this creates visual noise and provides no context to someone using a screen reader. Keeping link text short (but not too short[.](class-04.md)) is helpful, since it makes them easier to read, both for screen readers and visual users.

## CSS Layout

### CSS Layout: Normal Flow CSS Layout: Positioning

1. What is meant by “normal flow”?  
Normal flow refers to the way in which items are placed within the browser viewport. Block level elements are set on new lines depending on the block flow direction, and inline elements are placed on the same line as other content so long as there is room for it to do so.
2. What are a few differences between block-level and inline elements?   
Block elements span 100% of the parent element's width by default, and can have their width and height manipulated. They are placed on new lines. Margin collapsing applies to block elements. Inline elements sit on the same line alongisde other inline elements. If they overflow, they will wrap onto a new line, or just go to a new line completely if it is unable to wrap (like an image).
3. ___ positioning is the default for every html element.  
Static.
4. Name a few advantages to using absolute positioning on an element.   
Absolute positioning allows you to stack elements without affecting the placement of other elements. Absolutely positioned elements *do not exist* in the normal document flow, so they do not leave a gap where they "should" be. This can be used to create UI elements that do not disturb other parts of the page, such as pop-ups and drop-down boxes.
5. What is a key difference between fixed positioning and absolute positioning?  
They function almost the same. The difference is that absolute elements are positioned according to their nearest *positioned* ancestor. Typically, fixed elements are placed relative to the visible portion of the viewport, so that it is not affected by a page scroll.

## Learn JS

### Functions -- Reusable Blocks of Code

1. Describe the difference between a function declaration and a function invocation.  
A function must be declared somewhere before it can be used. Declaring a function defines it. The code inside of a function is *not* run at declaration. Invocation is also referred to as "calling" a function, and actually runs the function's code.
2. What is the difference between a parameter and an argument?  
While the terms are sometimes used interchangeably, parameter typically refers to the variable inside of the function definition. It acts as a placeholder, and thus has no actual value. An argument is what is given in place of the parameter when invoking/calling the function.

## Miscellaneous

### 6 Reasons for Pair Programming

1. Pick 2 benefits to pair programming and reflect on how these benefits could help you on your coding journey.  
     - Pair programming can help learners by exposing them to unique ways of solving a problem that they may not have thought of on their own. Each person's unique life experiences will drive them to solve problems in different ways, and "collecting" these ways of solving problems can be a great way of improving ones own skills.
     - Pair programming can help with interpersonal skills, but can also help a learner feel more comfortable *talking* about code. Job interviews often require pair programming, and even those that don't will require applicants to talk about coding in some way. Talking problems out in a learning environment can make the job interview process feel more natural.

## Things I want to know more about

I've never pair programmed. I'm very interested in participating in it and learning this skill!