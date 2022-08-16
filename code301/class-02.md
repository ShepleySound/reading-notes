# Class 02
This class introduces the ideas of state, props, and the React lifecycle.

## React lifecycle

1. Based off the diagram, what happens first, the ‘render’ or the ‘componentDidMount’?  
'Render' happens first, since a first render happens during the mounting phase, and 'componentDidMount' is called when the mounting phase is completed.
2. What is the very first thing to happen in the lifecycle of React?  
For components, the mounting phase begins, and the Constructor is called.
3. Put the following things in the order that they happen:  componentDidMount, render, constructor, componentWillUnmount, React Updates
    1. constructor
    2. render
    3. React updates DOM (and refs)
    4. componentDidMount
    5. ComponentWillUnmount
4. What does componentDidMount do?  
This is a method that is called when a component is finished mounting. It can be used to load things after the mounting phase completes such as subscriptions or network requests.  

## React State Vs Props
1. What types of things can you pass in the props?  
Props can be used to pass data from one component to another. It's like a function argument.
2. What is the big difference between props and state?  
Props are handled outside of the component they are passed into, whereas state is handled internally inside of the component itself.
3. When do we re-render our application?  
The application is re-rendered whenever the state of a component changes.
4. What are some examples of things that we could store in state?  
State can be used to store things like counters or data that is meant to be changed.

## Things I want to know more about
- I'd like to have a better understanding of state vs. props. I feel like I have a decent handle over the differences, but I definitely need more hands-on experience with them!