# Class 01

## Getting Started

1. **Compose a short poem describing how HTTP sends data between computers.**  
*Haiku*  
A client requests  
The server gives permission  
Files are now served
2. **Describe how HTML, CSS, and JS files are “parsed” in the browser.**  
The browser goes through the retrieved HTML file, and grabs references to any CSS and JS files using `<link>` or `<script>` tags. The browser makes sense of HTML and CSS files by building DOM trees and CSSOM structures, and executes the provided JavaScript.
3. **How can you find images to add to a Website?**  
Saving files from Google Images works, provided it does not violate copyright. I've found a lot of great images on Unsplash.com!
4. **How do you create a `String` vs a `Number` in JavaScript?**  
Wrapping a variable in quotations will create a String. Declaring a number without quotations will result in a Number.  
String - `let x = '10'`  
Number - `let x = 10`
5. What is a Variable and why are they important in JavaScript?  
Variables allow us to store data or values for later use.

## Introduction to HTML

1. **What is an HTML attribute?**  
An HTML attribute is placed inside of an element's opening tag, and defines additional features of the element outside of the primary content. Examples could be Class or ID (for organization and identification within the DOM), titles, sources for scripts/images, or hrefs for page links.
2. **Describe the Anatomy of an HTML element.**  
Elements typically are made up of an opening tag, content, and a closing tag. Not all elements have content or closing tags, such as `<img>` elements, and may just consist of an opening tag with any defining attributes included.
3. **What is the Difference between `<article>` and `<section>` element tags?**  
An `<article>` element is meant to be used for a portion of a document or application that can be distributed or reused on its own without further context. Content such as news articles, blog posts, or certain widgets make sense inside an `<article>` element. A `<section>` element is more generic, and is to be used for grouping semantically related content. Both elements should typically include a header before the main content.
4. **What Elements does a “typical” website include?**  
At a structural level, a typical website will include the following elements -  
   - `<!DOCTYPE html>` - Alerts the browser to the document type.
   - `<html>` - defines the root of an HTML document, and contains all other elements. Should include a `lang` attribute to assist browsers and search engines in determining the written language.
   - `<head>` - Contains the title, CSS links, and any metadata.
   - `<body>` - Includes the primary content of the page that will be displayed to the user.
5. **How does metadata influence Search Engine Optimization?**  
Having a `<meta>` title and description that contains keywords relating to your page's content can help search engines prioritize your page when deciding what to show to users, although these elements are not weighted as heavily as they used to be due to the practice of spamming keywords. They are still useful, as they determine what the user will see when the page appears in search engines, or on social media links if using specialized `<meta>` tags.
6. **How is the `<meta>` HTML tag used when specifying metadata?**  
Most `<meta>` tags include a `name` and `content` attribute, for specifying the type of meta element and the content of the meta element, respectively.

## Miscellaneous

### How to start to design a website

1. **What is the first step to designing a Website?**  
The first step in designing a website is project ideation, the process of figuring out what you want to accomplish and what resources you will use to begin accomplishing the required tasks.
2. **What is the most important question to answer when designing a Website?**  
"What exactly do I want to accomplish?" Beginning the design of a website with no end state or goal in mind is an easy way to hit a creative roadblock or misutilize technical resources.

### Semantics

1. **Why should you use an `<h1>` element over a `<span>` element to display a top level heading?**  
`<h1>` elements come with default styling that typically includes heavier font weight, larger font size, and a block display, which places the content on a new line. Using a `<span>` element would require unnecessary extra styling, and also ignores semantic best practices.
2. **What are the benefits of using semantic tags in our HTML?**  
Semantic tags help developers maintain proper organization while working on a website. They also help with Search Engine Optimization, separating different types of content from each other in a logical manner. Arguably most importantly, semantic tags help with accessibility, allowing tools such as screen readers to properly parse and navigate a website in ways that their users expect them to.

### What is JavaScript?

1. **Describe 2 things that require JavaScript in the Browser?**  
   1. JavaScript is required when dynamic or interactive content is needed. One example is prompting the user for input when pressing a button.
   2. Accessing an API, which allows the use of data, either internal or external, to perform tasks and operations. For example, grabbing a user's location using a geolocation API, using that data to request data from a weather API, and displaying local weather information to the user.
2. **How can you add JavaScript to an HTML document?**  
JavaScript can be added using a `<script>` element. The JavaScript can be placed inside the element (inline), or loaded from an external file using the `src` attribute.
