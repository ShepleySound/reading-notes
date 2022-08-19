# Class 05
This class goes over some higher-level React concepts such as SRP, the initial design process, and state management.

## React Docs - Thinking in React

1. What is the `single responsibility principle` and how does it apply to components?  
It means that, ideally, a function should only do one thing. If it grows past the scope of what it was designed to do, it should be "decomposed" into smaller pieces. This makes testing functionality much easier. Components should be treated in much the same way. If a component is handling too many "things", then reasoning about the structure of an application can get messy very quickly.
2. What does it mean to build a ‘static’ version of your application?  
A 'static' version of the application is one where there is no state or interaction built in. It's a step past a wireframe. The structure of the page and some styling is built out, which then lets the developer better decide where state management needs to happen.
3. Once you have a static application, what do you need to add?  
Once the static portion is done, `state` will need to be added. This helps us trigger changes on the page.
4. What are the three questions you can ask to determine if something is state?  
    1. Is it passed in from a parent via props? Not state.
    2. Does it remain unchanged over time? Not state.
    3. Can it be computed based on any other state or props? Not state.
5. How can you identify where state needs to live?  
It needs to be determined which components use the particular data, and then you find a common "owner" or parent component. That common parent, or a component higher up in the hierarchy, should own the state. If it doesn't make sense for any of the existing parents to own the state, then a new component can be created and added somewhere in the hierarchy above.

## Higher-Order Functions

1. What is a “higher-order function”?  
A higher-order function is a function that performs operations on other functions. This can mean either returning a function or taking a function as an argument.
2. Explore the greaterThan function as defined in the reading. In your own words, what is line 2 of this function doing?  

```javascript
function greaterThan(n) {
  return m => m > n;
}
let greaterThan10 = greaterThan(10);
console.log(greaterThan10(11));
// → true
```
This actually took me a while to figure out. I had to go through and add some console.logs to the code and really work through it. It's really interesting!  
Line 2 is actually *creating* a function. So `greaterThan()` is both a function call AND a function definition. Logging `greaterThan(10)` returns -
```
m => m > n;
```
This shows that we basically moved down into another function, and that we can pass in arguments after the previous definition. Woah!
```javascript
const greaterThan10 = greaterThan(10);
console.log(greaterThan10(11)) 
console.log(greaterThan(10)(11)) // THIS IS THE SAME THING AS THE LAST LINE!
```
3. Explain how either map or reduce operates, with regards to higher-order functions.  
`map()` is called on an array. It creates a new array and then applies a function to each element in the array it was called on, then pushes the returned value of that function to the new array.