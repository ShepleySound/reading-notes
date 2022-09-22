# Class 04

These notes will cover some fundamental questions about the differences between SQL and NoSQL databases, as well as some SQL modeling techniques.

## [nosql vs sql](https://www.thegeekstuff.com/2014/01/sql-vs-nosql-db/?utm_source=tuicool)

1. What type of database is the best fit for a complex, query intensive environment?  
SQL has a powerful, standardized query structure, and tends to be the best fit for situations where there will be many complex queries happening.

2. What type of database is the best fit for hierarchical data storage?  
There's a particular type of NoSQL database called a graph database that may be a better fit for storing data with hierachical relationships than a standard relational database.

3. Describe the differences in scalability between a SQl and NoSQL database as though you were speaking to a non-technical friend.  

There are many articles that flatly state that "SQL scales vertically (Adding more power), NoSQL scales horizontally (Spreading data out across more machines)". The reality is that there's a lot of really complex, underlying tech going on in both SQL and NoSQL databases, and not only is the tech always moving forward, but the limitations of some of these systems come down to how the individual databases are designed by administrators. One thing that is that most SQL databases have built-in structures in place to ensure consistency.  

We're going to make *a lot* of assumptions here, so don't take this as a concrete source of truth! In some cases, updating a NoSQL database is as easy as giving a command that says "Hey, find this thing and change it." or "Hey, throw this new thing on the pile." In contrast, updating a SQL database typically involves a lot of verification to ensure that the correct thing is happening. The database will "lock" certain things during operations to make sure that things don't get out of sync. SQL databases are also typically spread across different tables, and joining these tables together to reference related data can be pretty slow, relative to other operations that computers make. This problem becomes compounded if tables are spread across multiple machines, since this will typically require some sort of network connection. So by placing all of our tables on a single machine, we can speed up the process of looking up and performing operations across those tables. NoSQL databases, generically speaking, store all related documents on a single machine, so scaling *out* to multiple machines isn't as inefficient. There's quite a bit more complexity to talk about there, but that's a bit of the basics!

## [sql modeling techniques](https://www.essentialsql.com/get-ready-to-learn-sql-7-simplified-data-modeling/)

1. Among data tables, what is a one-to-many relationship and how do we “relate” them?  
A one-to-many relationship is one where rows are related between two tables. Specifically, table A will have a single row that may relate to multiple rows in table B. Table A might have "Customers", and table B might have "Orders". The Customer entry may have an "ID" column, which would relate to a column in table B called something like "Customer_ID". Using this design, we would be able to search for orders from a particular customer using their ID from table A, or find details for a particular customer using the Customer_ID from table B.

2. Prior to designing your relational database, it might be useful to ___ a ___ of the database tables and their relationships.  
It is often useful to create a diagram of the database's tables and their relationships, particuarly if those relationships are complex.

3. Explain the difference between a primary and foreign key.  
Using our previous example, the ID in the Customers table would be a primary key. The values in a primary key must be unique to that column, so multiple rows cannot share a value. The Customer_ID column in the Orders table would be a foreign key. Foreign keys can be repeated in multiple rows, and they match a primary key in another table.

## [sql vs nosql](https://www.youtube.com/watch?v=ZS_kXvOeQ5Y)

1. How do we treat keywords and parameters differently in SQL syntax?  
Keywords (Such as WHERE, SELECT, INSERT, etc.) are typically all uppercase. Parameters are typically lowercase. This makes SQL queries a bit more readable.

2. Define normalization within the context of schemas and data.  
Whew. So. Normalization can be described in terms of "Normal Forms". First, Second, and Third Normal Forms are common. There are a lot of resources about the different forms. [This is a great one.](https://www.simplilearn.com/tutorials/sql-tutorial/what-is-normalization-in-sql#:~:text=Normalization%20is%20the%20process%20to,data%20from%20the%20relational%20tables.) Essentially, normalization is a process in which we ensure that data is not unnecessarily replicated and that data is stored in a logical manner.

3. Explain the difference between one-to-one, one-to-many, and many-to-many relationships to a non-technical recruiter.  
When we talk about relationships in SQL, we typically are talking about relationships between entries in different tables.  

- In a one-to-one relationship, an entry in table A is referred to in a single entry in table B. This isn't very typical if we're being technical, since we typically want to confirm that the relationships actually exist. In many cases, a one-to-one relationship could probably better be described as a "one-to-none-or-one" relationship.
- One-to-many is a common type of relationship. This can happen in the case of a customer to order relationship. A customer will be defined as a single entry in table A, their orders will be in table B. Table B will have the relationship to a particular customer defined using a key (foreign key) that is equal to a unique key in table A (primary key).
- Many-to-Many relationships are typically created using three tables. Say we wanted to have a table of people, a table of books, and a way to see whether someone has read a particular book. By creating a third table with entries that point to book_id and person_id, we can reference our first two tables without unnecessarily duplicating data.