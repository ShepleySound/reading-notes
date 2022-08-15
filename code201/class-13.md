# Class 13

## Local Storage and How To Use It On Websites

1. Why would a developer use local storage for a web application?  
Local Storage allows developers to store data client-side, rather than on a server. This could work well for small web applications with data doesn't need to be stored and manipulated on a server, but that still needs to have *state*. It's easy to use, requires no complex setup for the developer, and allows a user to maintain data across browser refreshes.
2. What information should not be stored in local storage?  
User's personal information and passwords should not be stored in Local Storage. While it would seem that it's safe, as the data should typically remain on the local machine, it is still data stored as a string, and nefarious code running on a user's machine or in their browser could potentially transmit this data somewhere else. 
3. Local storage can store what type of data? How would you convert it to that type before storing?  
Local Storage stores data as an object, but the keys and values of this object can only be in string format. `JSON.stringify()` allows you to convert data to a String for storage, and `JSON.parse()` allows you to convert this data back into a format that JS will understand.