# Class 06

## JavaScript Object Basics

1. How would you describe an object to a non-technical friend you grew up with?  
Think of an object as defining something with a real-world analogue. For example, a dog. Every dog has qualities, attributes, and traits that make it a dog, but the *value* of those things is what makes it unique. Let's assume that every dog has fur, a tail, eyes, a name and a height. These can be defined as `properties` of a dog. So if I have 20 dog objects, I'll expect them all to have values attached to those properties, and I would also expect that they can be accessed in some way. <br>Objects also have `methods`, which define actions that the object can perform. All dogs can bark and fetch, so `bark` and `fetch` would contain blocks of code that define what happens when the method is called (or the action is performed). Furthermore, the method can reference the object's properties, so, for example, a dog's ability to `fetch` could in some way be affected by its `height`. 
2. What are some advantages to creating object literals?  
Object literals allow the quick creation of objects that do not necessarily need to be duplicated. In a game, a type of enemy should probably be built using Classes or some sort of constructor, but the object that defines attributes of the pause menu is, in a lot of cases, a one-off definition.
3. How do objects differ from arrays?  
Objects, like arrays, can hold literally any other type of data, but have the advantage of utilizing key:value pairs. Arrays are useful for data that needs to be iterable, like a list of names without any other context. Objects are not iterable by default, so they are more difficult to loop over, but they are very useful if it contains data that can be separated out into different properties.
4. Give an example for when you would need to use bracket notation to access an object’s property instead of dot notation.  
Bracket notation is necessary when an object's property is helpful if the property name is a string containing spaces, or a non-string number.
5. Evaluate the code below. What does the term `this` refer to and what is the advantage to using `this`?  
```
const dog = {
  name: 'Spot',
  age: 2,
  color: 'white with black spots',
  humanAge: function (){
    console.log(`${this.name} is ${this.age*7} in human years`);
  }
}
```  
`this` refers to the `dog` object. Inside the `dog` object, `this.name` is the same as referencing `dog.name` outside of the `dog` object. `this` allows us to play with scoping so as to dynamically reference things without needing to refer directly to the object variable name. It has many other uses, but that's one of them!

## Introduction to the DOM

1. What is the DOM?  
The DOM stands for `Document Object Model`. It is an object structured representation of a page that allows scripting languages (such as JavaScript) to manipulate a page.
2. Briefly describe the relationship between the DOM and JavaScript.  
The DOM provides properties and methods that are accessible through JavaScript and holds the data that JavaScript can manipulate. JavaScript can provide new data to the DOM, and the DOM will update in kind.
