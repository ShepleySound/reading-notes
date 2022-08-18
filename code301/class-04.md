# Class 04
This class goes over the idea of controlled components/forms in React as well as the Ternary operator in JavaScript.

## React Docs - Forms
1. What is a ‘Controlled Component’?  
A controlled component is a component that might typically have its state handled by its own existence as an HTML element, but that has been modified to accept React as a "single source of truth". So, instead of a text input tracking and updating its own value, we can have React pass it in as state.
2. Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why.  
We should update the state as soon as a response is entered. One reason is that we are passing the `value` of an `input` element in as state, so if we don't keep it updated `onChange` then the rendering of the newly entered text can start to get wonky (or just not change at all!) Another reason comes down to the philosophy of React. React wants to track the current state of an application and update/re-render the DOM whenever there is a change made. Letting user input change the DOM 'directly' and *then* passing that data into React later sort of breaks one of React's fundamental goals.
3. How do we target what the user is entering if we have an event handler on an input field?  
The `value` will come from `this.state.value`, so whatever React's state says the value is, that's what the `input`'s value will be. We use the onChange event handler and call `this.setState()` inside of the event handler. This tells the DOM that, whenever a valid change is entered, to call `this.setState()`, where we will grab the new value from the `event.target`.
This might seem backwards, since we're grabbing the new value from `event.target`... Why not just use the built-in way, letting the user type text and letting the browser handle changes? I believe this is because of how the `render()` function works. React is only going to call `render()` when it senses that a change to state has been made, so to properly allow React to handle its own world, we need to use state in this way.

## The Conditional (Ternary) Operator Explained
1. Why would we use a ternary operator?  
Because it's great! Just kidding. I mean, it is. But it dramatically simplifies `if/else` statements. If we know that we're dealing with a case that has cut-and-dry true/false conditions, it's much simpler to throw in a ternary operator than to write an entire `if/else` statement. It takes a bit to get the syntax engrained, but I find that I reach for it quite a bit now that I understand it better!
2. Rewrite the following statement using a ternary statement:

### Original Statement
```javascript
if(x===y){
  console.log(true);
} else {
  console.log(false);
}
```

### Rewritten Statement
```javascript
x===y ? console.log(true) : console.log(false)
// OR
const bool = x===y ? true : false;
console.log(bool)
```
