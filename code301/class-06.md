# Class 06
This class goes over node.js fundamentals and the importance of pair programming.

## [An Introduction to Node.js on sitepoint.com](https://www.sitepoint.com/an-introduction-to-node-js)

1. What is node.js?  
node.js is a JavaScript runtime that is built on top of Chrome's V8 Engine. It also has a package manager (npm) that allows for developers to manage dependencies and work with other libraries/frameworks.
2. In your own words, what is Chrome’s V8 JavaScript Engine?  
V8 is an engine that handles the compilation and execution of JavaScript code. It does not handle things like the DOM or Web API's. It provides the data types, operators, objects, and functions defined in ECMA.
3. What does it mean that node is a JavaScript runtime?  
This means that it handles the execution of code. It defines the environment in which the code is executed.
4. What is npm?  
npm, when it was first created, stood for Node Package Manager. It has since expanded in scope, so now just goes by "npm". It allows developers to write modules/libraries/frameworks, upload them to a central repository, and manage versions. It also allows developers to install from this repository and manage dependencies within their own programs.
5. What version of node are you running on your machine?  
v18.7.0
6. What version of npm are you running on your machine?  
8.17.0
What command would you type to install a library/package called ‘jshint’?
npm install -g jshint npm install executes npm and tells it to get ready to install something. -g tells it to install the module globally, so it can be used anywhere on the system. jshint tells it which module from the npm repository to install.
7. What is node used for?  
Node is used for back-end development and server-side scripting, but it is also used to build development environments and automate certain tasks that make developing applications easier, even if they don't require back-end manipulation.

## 6 Reasons for Pair Programming

1. What are the 6 reasons for pair programming?  
- Greater efficiency
- Engaged collaboration
- Learning from fellow students
- Social skills
- Job interview readiness
- Work environment readiness
2. In your experience, which of these reasons have you found most beneficial?  
I have found it very helpful in terms of building social skills and communication, particularly when it comes to talking about code. It's one thing to be able to write code, and another thing to be able to communicate your thoughts clearly, but communicating your code thoughts to someone else while they're working to fix a problem is another thing entirely. It's not enough to just relay the solution and the syntax involved, but you have to be able to explain the why behind your solution, and being able to do that can lead to a greater understanding of the underlying problem/solution.
3. How does pair programming work?  
Pair programming involves two people (hence 'pair'). One person acts as the navigator, and the other acts as the driver. The navigator determines the big picture of what gets focused on, and scans the code for any potential issues. The driver handles the actual keyboard/coding portion, and focuses on the task at hand while listening to the navigator for instructions and potential fixes.