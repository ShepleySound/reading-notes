# Class 03

These topics dive into organizational/list elements in HTML, the CSS box model, and some useful JavaScript concepts.  

## Learn HTML

### Ordered and Unordered lists.

1. When should you use an unordered list in your HTML document?  
An unordered list should be used when listing items with no particular order, or when the order in which the items are displayed is unimportant to the audience's understanding.  
2. How do you change the bullet style of unordered list items?  
The bullet style of unordered lists can be changed using CSS, specifically the `list-style-type` property.  
3. When should you use an ordered list vs an unorder list in your HTML document?  
An ordered list should be used when the order of the items in a list is important, such as when displaying steps in a recipe. An unordered list can be used when the order is unimportant, such as when displaying the ingredients of a recipe.  
4. Describe two ways you can change the numbers on list items provided by an ordered list?  
   - CSS has a property called `counter-reset`. This property not only affects auther-created counters, but also the counters used in HTML ordered lists.  
   - You can specify a `start` attribute in the `ol` opening tag, which will start the list numbering from the specified number.  

## Learn CSS

### The Box Model

1. Describe the CSS properties of `margin` and `padding` as characters in a story. What is their role in a story titled: “The Box Model”?  
```
The Wheel of Time turns, and Ages come and pass, leaving memories that become legend. Legend fades to myth, and even myth is long forgotten when the Age that gave it birth comes again. In one Age, called the Third Age by some, an Age yet to come, an Age long past, a wind rose above the misty peaks of HTML.*

Padding pressed against the content rising from the center of the Box, its origins known only to the Dark One. Sweat dripped down Padding's face as she struggled to hold her enemy at bay. The edges held firm, the content remaining separated from the border... For now.

Margin sat on the other side of the border, unaware of the struggle inside. Sitting in the shade of the Box, he eyed a fellow in garb similar to his own - a guard from a nearby element. Sometimes he mingled with the other guards. Where was the harm? Nothing would ever harm their Box.
```  
**Note** - The first paragraph comes from the opening of each book in Robert Jordan's *The Wheel of Time* series.  

2. List and describe the four parts of an HTML elements box as referred to by the box model.  
   - Content - Typically the center of the box, where things such as images and text are placed.
   - Padding - The transparent area surrounding the content.
   - Border - Surrounds the padding and the content.
   - Margin - The transparent area outside of the border. Clears space around the rest of the parts.

## Learn JS

### Arrays. Operators and Expressions. Conditionals. Loops.

1. What data types can you store inside of an `Array`?  
An `Array` in JavaScript can hold any data type. Data types can even be mixed inside of the same `Array`.
2. Is the people array a valid JavaScript array? If so, how can I access the values stored? If not, why?  

``` 
const people = [
  ['pete', 32, 'librarian', null], 
  ['Smith', 40, 'accountant', 'fishing:hiking:rock_climbing'],
  ['bill', null, 'artist', null]
  ];
```  
The array is valid. The inner arrays can be accessed using their indexes, and the individual values can be accessed using their indexes within the inner array they are located inside. For example, `people[1][1]` would access the `Number` 40 in the 2nd inner array.  

3. List five shorthand operators for assignment in javascript and describe what they do.  
   - `=` - Assigns the variable on the left to be equal to the right hand side of operator.
   - `+=` - Addition. `x += y` is equivalent to `x = x + y`
   - `-=` - Subtraction. `x -= y` is equivalent to `x = x - y`
   - `/=` - Division. `x /= y` is equivalent to `x = x / y`
   - `*=` - Multiplication. `x *= y` is equivalent to `x = x * y`

4. Read the code below and evaluate the last expression and explain what the result would be and why.  

```
 let a = 10;
 let b = 'dog';
 let c = false;

 // evaluate this
 (a + c) + b;
```  

The result would be a `String` that contains `'10dog'`. `a + c` is evaluated first, and the `Boolean` value is coerced into a `Number` because of the `+` operator and the lack of a `String` in the current statement. Since `false` coerces to `0`, the result remains the same, the `Number` `10`.  

Then, the rest of the expression is evaluated. `10 + 'dog'`. Whenever there is a `String` present alongside a `+` operator, it triggers coercion of other types in that expression to a `String`. The strings are then concatenated, or combined.  

5. Describe a real world example of when a conditional statement should be used in a JavaScript program.  
Conditional statements can be used to check whether the data provided by a user matches certain parameters that the program is expecting, or to show the user something different depending on their input.
6. Give an example of when a Loop is useful in JavaScript.  
Loops can be used to perform tasks multiple times. An `Array` containing a large list of data (such as names) could be printed to the screen. A continuous loop can be setup that is only "broken out of" whenever the user inputs data within a set parameter.

## Things I want to know more about

 - I *understand* the box model, but for some reason I often get mixed up when it comes to the differences between `content-box` and `border-box`. It's one of those things that I haven't used often enough to have completely memorized, but I reach for it enough times that I've noticed how annoying it is to have to refresh myself on it! Hopefully I can find some excuses to use it more often to get it better cemented in my head.