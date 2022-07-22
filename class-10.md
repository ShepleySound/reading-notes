# Class 10

## What Went Wrong? Troubleshooting JavaScript

1. Name some key differences between a Syntax Error and a Logic Error.  
A Syntax Error occurs when there are mistakes in the code that cause the program to break. This typically comes with error messages, and will stop the code from running at the point of error. A logic error will allow the code to run because there's not actually anything *wrong*, but the output will not be what is expected. Examples would be when you receive NaN when a number is expected, or when an infinite loop is accidentally triggered in a `while` loop because it isn't being broken out of.
2. List a few types of errors that you have encountered in past lab assignments and explain how you were able to correct them.  
Yesterday I was getting a logic error in my data validation. I was checking to make sure `min < max`, and sometimes my conditional worked as expected, but sometimes it didn't. `500 < 900` would be true, but `500 < 1000` would be false! Turns out, I wasn't parsing my strings, so JavaScript was doing its thing and only comparing the first 'digit' of the string.
3. How will this topic continue to influence your long term goals?  
Troubleshooting is a daily part of a developer's life, and knowing where different errors can occur will help to quickly resolve issues. It's helpful to know that sometimes the code isn't necesarily *wrong*, and that JavaScript is doing exactly what you've told it to do... But sometimes what you tell it to do and what you want it to do are different!

## The JavaScript Debugger

1. How would you describe the JavaScript Debugger tool and how it works to someone just starting out in software development?  
The debugger allows you to keep track of variables as the code runs and set breakpoints that will pause your code at certain places. For example, you could have it go through a loop line-by-line and watch the result of a counter variable over every single loop.
2. Define what a breakpoint is.  
A breakpoint is defined when debugging, and it is where the debugger will pause code execution.
3. What is the call stack?  
The call stack is a section of the debugger, but it's also an important part of the JavaScript interpreter. It determines the order in which code runs, especially pertaining to function calls. When a function is called, it is added to the top of the stack, and what is on the top of the stack is always ran first. So if a function is called inside of another function, the inner function is placed on the stack, ran, and then the outer function's code is continued.