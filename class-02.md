# Class 02

These topics continue establishing a foundational knowledge of HTML and CSS structure, as well as basic JavaScript syntax.

## Introduction to HTML

1. **Why is it important to use semantic elements in our HTML?**  
Semantic elements make it easier for users to find the information they are looking for quickly, and make developing a website quicker by helping to maintain proper organization. They also are important for accessibility tools and applications.
2. **How many levels of headings are there in HTML?**  
There are 6 levels of headings in HTML.
3. **What are some uses for the `<sup>` and `<sub>` elements?**  
`<sup>` creates superscripted text. According to MDN, `<sup>` "should only be used for typographical reasons". It should not be used purely for presentation or appearance. Proper uses of `<sup>` include exponents, ordinal numbers (such as "3<sup>rd</sup>"), and lettering in some languages. The same applies to `<sub>`, which creates subscripted text. Appropriate uses include footnote numbers and in chemical formulas.
4. **When using the <abbr> element, what attribute must be added to provide the full expansion of the term?**  
The `title` attribute allows the full expansion of the abbreviation, usually presented when hovering over the element with the mouse.

## Learn CSS

1. **What are ways we can apply CSS to our HTML?**  
CSS can be applied to HTML using inline styling (directly in an opening tag using the `style` attribute), internal styling (using a `style` tag in the `<head>` element), or external styling (referencing a .css file in a `<link>` element).
2. **Why should we avoid using inline styles?**  
Not only do inline styles create messy HTML, they also carry the highest "weight" when compared to any of the CSS selectors, meaning that inline styles will override any internal *or* external CSS. This behavior could result in unintended consequences when styling a page, and can prevent the creation of a unified design without the use of extensive code repetition. 
3. **Review the block of code below and answer the following questions:**  
```   
h2 {  
  color: black;  
  padding: 5px;  
}
```

  - **What is representing the selector?**  
  `h2`, a type selector.
  - **Which components are the CSS declarations?**  
  The two lines `color: black;` and `padding: 5px;` are each CSS declarations. They each include a property (`color` and `padding`) and a value (`black` and `5px`) in property:value pairs.
  - **Which components are considered properties?**  
  `color` and `padding`.

## Learn JS

1. **What data type is a sequence of text enclosed in single quote marks?**  
`String`
2. **List 4 types of JavaScript operators.**  
   - Arithmetic Operators (`+`, `-`, `*`, `/`, etc.)
   - Comparison Operators (`>`, `<`, `>=`, `<=`, `!==`, `===`, etc.)
   - Logical Operators (`&&`, `||`, `!`)
   - Assignment Operators (`=`, `+=`, `-=`, `**=`, etc.)
3. **Describe a real world Problem you could solve with a Function.**  
A function could be created to convert US Dollars to a different currency, or convert different units of temperature measurement.

### Making Decisions in Your Code - Conditionals

1. **An if statement checks a __ and if it evaluates to ___, then the code block will execute.**  
condition (or expression), `true`
2. **What is the use of an else if?**  
`else if` allows for checking against another condition if the previous condition evaluates to `false`.
3. **List 3 different types of comparison operators.**  
Greater than (`>`), equal value AND equal type (`===`), greater than or equal to (`>=`)
4. What is the difference between the logical operator `&&` and `||`?  
`&&` returns `true` if the expressions on BOTH sides of the operator evaluate to `true`. ``||`` returns true if ONE of the expressions on EITHER side of the operator evaluate to `true`.