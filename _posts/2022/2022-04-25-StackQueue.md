---
title: Stack & Queue
date: 2022-04-25 11:31:30
categories:
- Javascript
tags: Basic Review Stack Queue
---

# Introduction
Today we will go over two of the most basic data structures, which are stack and queue!

# What is Stack?

- Stack is a linear data structure and has a characteristic of LIFO (Last in Last Out). LIFO means what was put in at the end comes out first. Think of stack of dishes: The dish you put on the top at the end is the first one you take. 
- **Push** is used to put in data, **pop** is used to take out data, and **peek** is used to take a look at the data that was put in at the end. 
- Stack is often used to access previous work or data. 

## Stack Methods

- pop(): Remove the top/last element of stack. 
- push(): Add an element. 
- peek(): Return the most recently added element to the stack. 
- empty(): Check whether a stack is empty. Return a boolean value.
- swap(): Swap elements in stack. 

### Pseudocode for Stack

1. Create a new class
2. Make an empty array with Constructor (set this)
3. Make a **push** function to push an element to an empty array.
4. Make a **pop** function to return the last element in the array.
5. Make a **peek** function that returns the element at -1 index of the array.




![](https://images.velog.io/post-images/rlcjf0014/bd847c80-0abb-11ea-ac09-01f2ebe054b1/20191114201403.png)

![](https://images.velog.io/post-images/rlcjf0014/c2553e70-0abb-11ea-ac09-01f2ebe054b1/20191114201522.png)

![](https://images.velog.io/post-images/rlcjf0014/c5801890-0abb-11ea-ac09-01f2ebe054b1/20191114201554.png)

![](https://images.velog.io/post-images/rlcjf0014/c7d13480-0abb-11ea-a410-d9a5cffe352b/20191114201612.png)


# What is Queue? 

- Queue is a linear data structure and has a characteristic of FIFO (First in First Out). FIFO means the data put in first comes out first. Think of a line at a restaruant or an amusement park. 
- **Enqueue** is putting data in and **Dequeue** is taking data out. 
- Queue is often used as a buffer that temporarily saves work that has to be done in an order. 

## Queue Methods

- enqueue(): Add an element
- dequeue(): Remove an element
- peek(): Return the first element of queue
- isEmpty(): Check if a queue is empty. Return a boolean value. 
- printQueue(): Return all elements of queue.

### Pseudocode for Queue

1. Create a new class
2. Make an empty array with Constructor 
3. Make a **enqueue** function that pushes an element to an empty array.
4. Make a **dequeue** function to shift element from an array.
5. Make a **peek** function to return the element at 0 index.
6. Make a **isEmpty** function that will check the length of an array and return true if 0 and false otherwise.
7. Make a **printQueue** function that returns all the elements in the array.

   
![](https://images.velog.io/post-images/rlcjf0014/d1423280-0abb-11ea-ac09-01f2ebe054b1/20191114201808.png)

![](https://images.velog.io/post-images/rlcjf0014/d3742db0-0abb-11ea-ac09-01f2ebe054b1/20191114201824.png)

![](https://images.velog.io/post-images/rlcjf0014/d4df2f60-0abb-11ea-ac09-01f2ebe054b1/20191114201850.png)

![](https://images.velog.io/post-images/rlcjf0014/d877bf70-0abb-11ea-ac09-01f2ebe054b1/20191114201902.png)

# Conclusion

Stack and Queue are often used and two of my favorite data structures. 
Know them well enough to use them whenever!









 





