# Data Structures and Algorithms
Data Structures and Algorithms are important concepts to understand when it comes to solving problems with code. Here's some questions involving DSA:

1. **What is 1 of the more important things you should consider when deciding which data structure is best suited to solve a particular problem?**  
An important thing to consider is the potential scale of the problem, as this will determine how the problem should be approached. A problem that is known to not require scalability can be solved using simpler data structures and can require less code. On the other hand, a problem that has the potential to scale (say, performing operations over millions or billions of data points) may require more care over the type of data structure implemented to ensure that the time and space complexities are reasonable.
2. **How can we ensure that we’ll avoid an infinite recursive call stack?**  
Recursive functions should typically have a *base case* or *halting case* that will determine the conditions in which the function will not call itself again.