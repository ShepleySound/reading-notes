# Class 07
This class goes over basic concepts of REST.

1. Who is Roy Fielding?  
Roy Fielding is one of the main authors of the HTTP spec and the creator of the REST architectural style.
2. Why don’t the techniques that we use today work well when we need to be able to talk to all of the machines in the world?  
I think this question is a bit interesting when considering today's tech, considering the original article was written almost 2 decades ago (I think... Maybe more)! REST is much more popular, and helps to standardize the issue of knowing whether or not a client requesting data is a machine or a human.
3. What is the HTTP protocol that Fielding and his friends created?  
HTTP is an application layer that lets systems talk to each other in a standardized way. It allows data to be transmitted between a client and a server (or any two machines, really) over the internet.
4. What does a GET do?  
A GET retrieves representation or resources. It does NOT modify any of that information.
5. What does a POST do?  
POST creates new resources.
6. What does PUT do?  
PUT updates an existing resources. An API can choose to allow a PUT to create a resource if it does not already exist.
7. What does PATCH do?  
PATCH partially updates an existing resource. PUT can also do this, but PATCH is considered to be the "correct" way, whereas PUT is intended to replace a resource in its entirety. 