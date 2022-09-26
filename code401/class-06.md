# Class 06

These notes will cover some fundamentals of authentication and authorization.

## [Securing Passwords](https://thehackernews.com/2014/04/securing-passwords-with-bcrypt-hashing.html)

1. Explain to a non-technical friend how you would safely hash and store a password.  
Hashing takes a text password and puts it through a complex algorithm. There are many different algorithms out there. The algorithm takes your readable text and turns it into an unrecognizable series of numbers and letters. Salting is an extra step that can (and should!) be added. Hashing can be beaten by bad actors, because the output is always the same for a certain input. If my password is "password123", and the hashed password is "jfkd49kdj939582kdfj1035485sjk", then all someone has to do is find the hashing algorithm and try random inputs until they get an output of "jfkd49kdj939582kdfj1035485sjk". Salting adds a random series of numbers and letters (called a salt) to your plain-text password and then hashes the combination. Because only you know your password and only the authentication service knows which random series was used as a salt the chances of both being guessed and decrypted are much lower.

2. What is Bcrypt?  
Bcrypt is a hashing function/algorithm that was published in 1999. It incorporates a salt, and is also adaptive in that an iteration count can be increased to make attacks against the stored hashes more difficult.

3. Why might you use something like Bcrypt?  
Hashing functions can be used when storing passwords in a database. A website may want to store users in its database and need some way to authenticate them, and hashing the passwords provides a layer of protection for user's information if a database were to be accessed by bad actors.

## [Basic Auth](https://en.wikipedia.org/wiki/Basic_access_authentication)

1. What is Basic Authentication?  

2. What properties are necessary in the header of a Basic Auth request?  
3. How are username:password in Basic Auth encoded?  

## [OWASP auth cheatsheet](https://www.owasp.org/index.php/Authentication_Cheat_Sheet)

1. Define the authentication process to a non-technical recruiter.  
2. How should your error messaging respond (both HTTP and HTML)? Why?  
3. Bookmark this link also and consider OWASP fundamentals any time you interact with authentication. Applications developed with security in mind from inception have fewer vulnerabilities throughout their lifecycle.  