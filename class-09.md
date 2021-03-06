# Class 09

## HTML Forms
1. Why are forms so important in web development?  
Forms allow website creators to get easily parsed input from users in a standardized format.
2. Forms should be easy to read, properly labeled, and should not break accessibility features. Forms provide a lot of different elements, and taking advantage of all of them helps users fill them out in ways that they are used to and expect!
3. List 5 form elements and explain their importance.  
   - `<form>` is the parent element of every form. It has attributes that handle different aspects of a form, such as what happens when it is submitted and where data should be sent.
   - `<label>` is attached to parts of the form to, of course, label them. the `for` attribute allows it to be attached to an element using the element's `id`, or the element can be nested inside of the `<label>` to connect them. The label is programmatically attached to the element as well as visually attached. Clicking on the `<label>` will shift focus to its attached element!
   - `<input>` takes user input. It has multiple attributes that help it connect to a script and to make it more user friendly. The `name` attribute identifies a variable name that will allow a scripting language such as JS to grab the `<input>` from its parent form. The `type` attribute identifies different input types that control certain parts of data validation as well as the way it is displayed to the user. The `value` attribute can be used to grab the user's input into the element.
   - `<fieldset>` creates a grouping of form elements that can be easily styled and that are accessible using assistive technologies.
   - `<legend>` acts as a label/header for the `<fieldset>` element. Some screenreaders will read out the `<legend>` content before it reads out each `<label>` to the user to provide further context.

## Learn JS
1. How would you describe events to a non-technical friend?  
Events are anything that *happens* on a webpage. This could be something that you do as the user, such as clicking on something, scrolling, or even hovering over something. It could also be something that happens as a side-effect, such as the page finishing a load process or an error occuring.
2. When using the `addEventListener()` method, what 2 arguments will you need to provide?  
The first argument is the type of event that is being listened for (such as `'click'`). The second argument is the code that is run whenever the event is triggered.
3. Describe the event object. Why is the target within the event object useful?  
The event object defines something that takes place inside of the DOM. It has a `target` property that holds the DOM element that the event listener was called on. This is useful because it allows us to reference data inside or to change something about the `target` element.
4. What is the difference between event bubbling and event capturing?  
Event bubbling happens inside-out, starting at the child element and bubbling up through the highest ancestor element. Capturing starts at the highest ancestor (usually `<html>`) and moves down through the hierarchy.


