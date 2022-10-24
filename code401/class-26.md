# Class 26 - React and Component-Based UI

## React Basics

### 1. What are the building blocks of a React app? 

The building blocks of React are *components*, which are pieces of a UI that contain their own logic and appearance. Components can be anything, from buttons, to forms, to entire pages!

### 2. What is the difference between an element and a React component?  

In React, there are *components*, *instances*, and *elements*.  

- A component is the primary building block of React. It defines the logic and appearance of a piece of a UI.
- An instance is what is created when a component is rendered.
- An element is a description of the instance that is to be created. It's a simple object that contains things like type, key, props, and children. It has no methods of its own.

### 3. What are some advantages of React’s component based architecture?  

Component-based architecture provides multiple advantages. First, it allows us to build visually and logically consistent UIs without too much effort. Second, it allows us to use those UIs pretty easily! Do we have a page that needs 50 buttons on it, all with the same style and that interact with our data in some way? Easy. Oh, you want 8 of the buttons to be blue and the other 42 to be green? We can do that, too.

## JSX Basics

### 1. What is JSX and why do we use it?

JSX is a markup syntax. It looks like HTML, but has stricter rules and slightly different syntax. We use JSX because it's easier than calling methods like createElement() manually.

### 2. Describe the process of embedding JavaScript expressions in JSX.  

JavaScript expressions can be embedded into JSX by placing them inside a pair of curly brackets {}.

### 3. Is it safe to embed user input in JSX? Explain.  

Yes. React DOM automatically escapes values embedded in JSX. In addition, everything is converted to a string before being rendered.

## Rendering Elements

### 1. Explain what a React Component is to a non-technical friend.

A component can be... a lot of things. But in its simplest form, think of a button on a page. What does this button look like? Maybe it's got a blue background, rounded edges, and white text. What does it do? Maybe it acts as a link to another page, or maybe it just makes a counter go up.

What if we want multiple buttons? Well, hooking all of the logic up for a single button can get pretty complicated. Components let us define what a button might look like and how it might act, and then we can use those components later. We could create a Button component that can take in any color as its background. Then, with a single line of code, we could create an *instance* of that button with whatever background color we want. What's more, we could create as many of those buttons as we'd like, and they can all be unique.

### 2. Describe mutability and React Components, specifically, how is the UI updated?

React really, *really* recommends that state is treated as read-only and immutable. This means that we should not directly change the value of an object in state, even if it *technically* works.

React offers methods to change state, such as the `useState()` hook. To update the UI, React checks to see if there are any differences between the previous state and the new state. If so, a rerender occurs.

### 3. If changes are made to the UI, what does React update?   

React updates the DOM, but only the parts of the DOM that change between renders. This is opposed to rerendering the entire page everytime something needs to update.
