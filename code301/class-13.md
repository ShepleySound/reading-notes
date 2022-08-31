# Class 13

## CRUD Basics

1. Which HTTP method would you use to update a record through an API?  
It depends. The PUT method updates an entire record, whereas PATCH sends a partial update to a record. Some people use PUT for everything, though!
2. Which REST methods require an ID parameter?  
DELETE, PUT, and PATCH require an ID parameter to ensure they are pointing to a particular record.

## [Speed Coding: Building a CRUD API](https://www.youtube.com/watch?v=EzNcBhSv1Wo) (Notes on the video)

1. What’s the relationship between REST and CRUD?  REST is a specified structure that data and its structures should follow. It specifies the GET, POST, PUT, PATCH, and DELETE operations. CRUD is a model for building applications, where its operations roughly map over the REST model/spec. CRUD stands for Create, Read, Update, Delete.

2. If you had to describe the process of creating a RESTful API in 5 steps, what would they be?  
    1. Create a server and database. Verify a connection to it them.
    2. Define the routes that will need to be connected to, along with the REST operations that you will be using on each route.
    3. Define any schemas that your data will need to adhere to.
    4. Have your routes perform REST operations on the database using proper validation.
    5. Test your REST operations!