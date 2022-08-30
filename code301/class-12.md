# Class 12

## [Status Codes Based On REST Methods](https://www.moesif.com/blog/technical/api-design/Which-HTTP-Status-Code-To-Use-For-Every-CRUD-App/)

1. In your own words, describe what each group of status code represents:

    - 100's: Informational codes. These typically deal with the header of the request.
    - 200's: Success! These codes deal with telling the client that a request has been accepted.
    - 300's: Redirect. These tell the client that whatever they are expecting/requesting is no longer at the requested destination, and instructs the client to issue a new request to a different location.
    - 400's: Client errors. These detail invalid requests to a server. This could be a timeout, an incorrect URL, or missing authentication.
    - 500's: Server errors. This could be due to overwhelmed servers, or it could be related to an exception that a client request triggers on the server.

2. What is a status code 202?  
Used for asynchronous processing. It says that the request was valid, and that a response with the processing of the request will finish at some point in the future.
3. What is a status code 308?  
Permanent Redirect. This instructs the client to use a new URL for this request, and to no longer use the current URL.
4. What code would you use if an update didn’t return data to a client?  
Code 204. This response will contain no data, and is good for things like simply saving an edited document.
5. What code would you use if a resource used to exist but no longer does?  
Code 410. This tells the client that the resource used to exist. It still could, but we don't know where it was moved if it does.
6. What is the ‘Forbidden’ status code?  
Code 403. It means that the client has authenticated or doesn't require authentication, but that it still does not have the correct authorization to perform the given request. The difference between authorization and authentication are interesting here, especially considering Code 401 is called "Unauthorized" in the spec.

## Build A REST API With Node.js, Express, & MongoDB

1. Why do we need to pull our MongoDB database string out of our server and put it into our .env?  
So that we can securely connect to the database without directly exposing a URL containing our database authentication information in the code.
2. What is middleware?  
Middleware is a function that has access to the `request` object, `response` object, and `next` function in the app's req-res cycle.
3. What does app.use(express.json()) do?  
`app.use()` allows us to use middleware. `express.json()` allows our server to accept JSON as a body.
4. What does the /:id mean in a route?  
`:id` is a parameter called `id`. It allows us to pass in a route with a currently unknown ID.
5. What is the difference between PUT and PATCH?  
PUT updates all of the information in a document. This is used a lot, even when only one thing is being updated, but I don't believe it's considered best practice. PATCH only updates the necessary, passed in information.
6. How do you make a default value in a schema?  
The `default` property allows us to create a default value.
7. What does a 500 error status code mean?  
500 error means that there's an error on the server, rather than something being directly the fault of the client.
8. What is the difference between a status 200 and a status 201?  
200 means "everything" is successful. 201 is more specific, and means that something was successfully created.