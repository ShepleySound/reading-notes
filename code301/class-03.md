# Class 03
This class expands on different ways of working with arrays and other iterables in JavaScript and, by extension, React.

## React Docs - lists and keys
1. What does .map() return?  
.map returns a new array, with each element in that new array being the result of the callback function. The new array is always the same length/size as the old array.
2. If I want to loop through an array and display each value in JSX, how do I do that in React?  
Assign Array.map() to a variable, and then pass some component's JSX in as a callback function. The return from the .map() can now be placed inside of another piece of JSX. This creates multiple components.
3. Each list item needs a unique... Key  
4. What is the purpose of a key?  
Here, the key acts similarly to how a primary key in a database functions. It ensures that the component/object/entry is unique in some way. If a component with the same key as another component is passed into a list, then it will replace/update the old component.

## The Spread Operator
1. What is the spread operator?  
It is an operator in JavaScript (ES6). Its primary use is in "expanding" an array into a list of arguments in a function call.
2. List 4 things that the spread operator can do.   
    - Adding to state in React
    - Combining objects
    - Copying an array
    - Spreading an array to be used as arguments in Math functions.
3. Give an example of using the spread operator to combine two arrays.
```javascript
const arrayOne = [1, 2, 3];
const arrayTwo = [4, 5, 6];
const combinedArray = [...arrayOne,...arrayTwo];
console.log(...combinedArray) // 1 2 3 4 5 6
```
4. Give an example of using the spread operator to add a new item to an array.
```javascript
const arrayOne = [1, 2, 3];
const newArray = [...arrayOne, 4, 5];
console.log(...newArray) // 1 2 3 4 5 
``` 
5. Give an example of using the spread operator to combine two objects into one.
```javascript
const objectOne = {wheels: 4};
const objectTwo = {color: 'red'};
const objectThree = {transmission: 'manual'};
const car = {...objectOne, ...objectTwo, ...objectThree, model: 'Mazda 3'}
console.log(car) // {wheels: 4, color: 'red', transmission: 'manual', model: 'Mazda 3'}
```

## How to Pass Functions Between Components
1. In the video, what is the first step that the developer does to pass functions between components?  
The dev creates a method called "increment" that will eventually be passed in.
2. In your own words, what does the increment function do?
It iterates over the `people` array and increments the `count` of the element whose `name` property matches the `name` argument.
3. How can you pass a method from a parent component into a child component?  
It gets passed in as props, and can then be used in the child component's `render()` function.
4. How does the child component invoke a method that was passed to it from a parent component?  
In this case, the method from the parent component is called inside of a method defined the child component. To invoke it, this new method is called using an event listener (`onClick`) inside the component's `render()` function.
