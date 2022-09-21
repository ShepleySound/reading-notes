# Class 03

These notes provide a brief review of ES6 classes and routing inside of Express.

## [Review: ES6 Classes](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)

1. Classes are a template for creating ____.  
Objects!
2. Can a class declaration be hoisted?  
Yes, class declarations in JavaScript are hoisted. It isn't always recommended to rely on hoisting, as it may be cleaner to better organize the code.
3. How would you describe a constructor and contextual “this” to a non-technical friend?  
So, we have to first understand what classes and objects are.

First, objects... At a very basic level. Imagine objects as just representing a *thing*. It could be a car, or a dog. Objects have `properties`, which are like attributes of the thing. They also have `methods`, which are like actions that the thing can do. But we'll just worry about properties for now.  

So, we could say that we have a car, and that car has a color, a make, a model, and a number of wheels. And we can define that car by just creating objects with those properties in code. That's pretty easy. But what if we want 5 of them? or 500 cars, all with different models and colors? Copy-pasting code gets inefficient and annoying quickly, so how do we solve this?

One way is with a *class*. With a class, we can define the *shape* of an object. See, classes get defined in code, but that definition doesn't really *do* anything. It's just a blueprint. Inside of the class is typically what's called a *constructor*, which takes in parameters, which you can think of as placeholders for values of things.  

After defining the class, we can use it to create new objects, and it uses its constructor to do so. Those parameters I mentioned are important here. They're what allow the newly created object to be unique. So say we have a class, or a blueprint, for a car. We might add in a lot of properties that all cars have inside the class. Does it have an engine? Seats? Seatbelts? A steering wheel? 4 wheels? Add it all in. But what about those unique parts of a car? The color, the make, and the model (lets imagine these are the only things that make a car unique...)  

When we create an object using a class, we'll feed the value of those things to the `new Car()` method. That might look like `new Car('red', 'honda', 'civic')`. We can do that because in the constructor we will have created those placeholders, and one of the things we have to do is use `this`.  

Okay, final big explanation - `this` is a term that tells a class "hey, I belong to a certain instance of a thing, not just to ALL of the things!". Oddly enough, saying color = 'red' inside of a class doesn't tell it much. It doesn't know what in particular to assign that color to. In code, we have to be very explicit in what we tell it to do. So we use `this` inside of the constructor/definition, and it knows that, whenever it sees the `this` keyword, we want it to reference the actual object that's being built, rather than the class itself.

## [Using Express Routing](https://expressjs.com/en/guide/routing.html)

1. Within Express, what does routing refer to?  
Routing is the way that the server/application's endpoints respond to requests from a client.

2. What is the difference between a route path and a route method?  
A route path is a string, string pattern, or regular expression. It determines the URL portion of the endpoint.  
A route method is derived from one of the HTTP methods. Along with the path, methods define the endpoint and how it responds to requests.

3. When is it appropriate to add next as a parameter to a route handler and what must you do if next has been passed to your middleware as a parameter?  
A route handler should have next as a parameter if it is going to function as middleware, or if there is going to be another callback/handler that follows. If next is passed in so that a handler can be used as middleware, next() must be called at the end of the handler.

## [Express Routing](https://scotch.io/tutorials/learn-to-use-the-new-router-in-expressjs-4)

1. What is an Express Router?  
Express Router is a "mini express application" that just handles routing. It allows us to create modularized routing. For example, we could define a router that points to the /protected route, so that all of its endpoints follow that route. We can also use it to apply middleware to routers.

2. By what means do we initialize express.Router() in an express server?  
We define a variable like `const router = express.Router();`. This tells express to create a new router that can be referenced.

3. What do we use route middleware for?  
We can use middleware to perform functions on each request, or we can call middleware to only perform functions on certain requests. An example of the first would be a logger function that logs out details of every request made to that router. An example of the second would be a piece of middleware that only validates whether a /person route has received a "name" in its query object.
