# Class 07

These notes cover JWT's and the basics of bearer authorization.

## [Intro to JWT](https://jwt.io/introduction/)

### 1. What is a JSON Web Token (JWT)?  

A JWT is a token in JSON format. It comes in 3 parts -

  1. Header (contains the signature encryption algorithm)
  2. Payload (contains information about the user or client)
  3. Signature (contains an encrypted version of the Header and Payload. The encryption is typically done using a secret key which is known only to the issuing service/server)  

### 2. When should we use JSON Web Tokens?  

JWT's can be useful in many situations. One situation in which they can be used is when we have multiple sessions/applications in which we want to share user authentication. We can issue a user a JWT on sign-in and verify it on each of our application servers.

### 3. Claims are expected in which structural component of a JWT?  

Claims are placed in the payload of the JWT.

## [Are JWTs Secure?](https://stackoverflow.com/questions/27301557/if-you-can-decode-jwt-how-are-they-secure)

### 1. If I get a JWT and I can decode the payload, how can we call that secure?

Ideally, the payload will not contain any sensitive information, such as the username or password. The encoding of the header and payload are not directly responsible for the security of the JWT. The security comes in the receiver's validation of the JWT. The receiver knows the secret that it uses to encrypt the JWT's signature, and so can rehash the payload and check to see if the result of that hash matches matches the received JWT's signature.

### 2. If sending a JWT, what must sender and receiver both know? Hint, it’s appended in the signature.

When using a signed JWT, the sender and receiver must both know the secret so that the client can sign the JWT using the secret key and the receiver can check against the known secret.

### 3. Explain how concatenated content and secret can be sent and received securely to a non-technical recruiter.  

Okay, so one key thing to note is that, when we are talking about sending sensitive information over the internet, we are typically already applying a layer of security in the form of HTTPS. You've probably seen this in your browser. Some browsers today will display a small lock symbol in your address bar to let you know this is being used on the site you're browsing.

When we use bearer auth with a JSON Web Token, we have the server create the JWT on signin/signup and give it back to the client. The client can then give that token BACK to the server when it wants to make a request for information. The server makes sure that the token it issued matches the token it receives, and if they are the same, the request is fulfilled. This JWT gets passed back and forth.

Okay, so we know that our information is relatively secure in transit, but nothing is foolproof, right? What if someone can grab our JWT, change some of the payload information, and pass it along to the server? Say the server is reading your phone number or email from the JWT to determine where to send a MFA message or a password reset link. (Hint: please don't do this... But what if?)

Well, the server has a secret. And in this case, only the server knows that secret. When the server created the JWT, it used your data, combined it with that secret, and then encrypted it using something called a hashing algorithm ([read more about that here](./class-06)). This hash gets appended to the JWT as the `signature`.

When the server receives a JWT, it does the same thing. It takes the payload, combines it with its known secret, and hashes it. Then it checks this new hash against the `signature`. If anything has changed in the payload, the signatures won't match!

## [JWTs Explained](https://www.youtube.com/watch?v=926mknSW9Lo)

### 1. JWT is Compact and self-contained. Describe how this is useful to a non-technical friend.  

When we use JWT's, we're passing them between the client and the server every time a request is made. Imagine that this happens every time you click a link on a page. If JWT's were large, this would slow the page down. Wouldn't that suck? We want things to be secure, but we don't want security to get in the way of things feeling fast and frictionless!  

Cool, so we take all of the information that we want the server to know about us and we put it in a nice little package. Just a string of text, not very long at all. What's better is that, not only does the JWT tell the server who we are, but it also _proves_ to the server that we are who we say we are!

### 2. What are the three components (the structure) of a JWT signature?  
A JWT signature is created by concatenating/combining the - 

    - base64-encoded header of the JWT
    - base64-encoded payload of the JWT
    - secret

The combination of these three things is then hashed with a hashing algorithm.
