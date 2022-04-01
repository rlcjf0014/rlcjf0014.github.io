---
title: Introduction to Data Structure and OOP
date: 2022-03-31 11:31:30
categories:
- Javascript
tags: Basic Review OOP DataStructure
---

# Introduction

It's been a while since I blogged, but like I always say, I will try to blog more regularly!

# **Data Structure**

#### What is data structure?

- A way to efficiently create, manage and save data
- Functions to present the formation, the relationship and application of data

Ex) Stack, queue, linked list...


### **Algorithm**

- A step-by-step list of directions to follow to solve a problem

1. Establish the rules of the problem
   - Define the inputs and outputs
   - Carefully establish the constraints of the problem
2. (If using TDD) Write a test that would verify a solution
   - vague senses of what you might need => specific test of what you want
3. Explore the problem space and discover techniques
   - consider edge cases (surprising or unlikely)
   - identify archetypes and common patterns
4. Generate a simple plan that should solve the problem
   - must be able to articulate the solution to a problem in plain language(I guess pseudo code)
5. Elaborate the plan into steps (pseudocode)
   - with indents to establish hierarchies
6. Optionally, verify each step in the process manually/mentally for some simple input
   - consider simple and ede cases
7. Transform pseudocode into real code


### **Intro to OOP** (Object Oriented Programming)


_**Computer Programming**_

- Computer programming refers to commands to give orders to a computer! Programming language makes software engineering possible. 
There are three types of programming language. 


1. **_Machine Languages_**
   - This is the most primitive language of computer, made of 1s and 0s. One mistake or a wrong number will fail the program. 

2. **_Assembly Languages_**
   - This is a programming languag a little easier than machine language. There are 10~ish keywords and the language is made up of basic commands. If you want to have fun with CPU, use this language! 

3. **_Programming languages_**
   - This is a more complicated programming language. Using a compiler, the assembly language will be converted to programming language.   

Ease of Implementation, Flexibility, Portability (Low to High) vs Speed of Execution, Code Density, Machine Specific (High to Low)

**_High-Level Languages_** - Type of Programming Language

- In a high-level programming language, the code is read from left to right. 
The interpreter reads the code and executes the program. 

- Two groups 

  - Procedural languages (C)
    - Initial high-level languages are Procedural language, which means they focus on structure and carries out commands line by line.  

  - Object-Oriented languages (OOP)
    - Uses a blueprint called "class". 
     - Java, C++, C#, Python, PHP, JavaScript, Ruby, Perl
     - Javascript is also object oriented. 

  #### **OOP*****

  - OOP was covered slightly in an older post, but we will go deeper into it!
  - Object oriented programming is a computer programming paradigm and one of the philosophies. 
  - It structures the logic through abstraction of data, creation of objects with properties and methods and flexible interaction of objects.
  - A class can create numerous instances (Objects).


    **Advantage**

  - **Code Reusability**: You can inherit and edit classes you did not make.

  - **Easy Code Maintenance**: All the variables, properties and methods will be in a class so you do not have to go line by line to fix an error. Just find that part in class and edit!  

  - **Great for Big Project**: You can divide the project into different modules using class so that many can work independently on a project at the same time.

  ​        
    **Disadvantage**

  - Slower process speed. 
  - As the number of objects increase, there is more memory allocated.
  - Takes a lot of time

  - **Classes and Objects**

    - A class is a prototype, idea and blueprint for creating objects. A constructor creats an instance. 
    - An object is an instance of a class. It's the actual data allocated to actual memory. 
    - When there is a class "car", color, price and speed are properties and moving forward and backward are methods. 

  - ### **OOP Basic Concepts**

    - **Encapsulation**: Like the title, all the properties and methods are encapsulated in a class. Everything is organized and tied into a class. For OOP, a class has all the information so as more instances are created, the program becomes more complicated. Using instantiation to expand the encapsulated class reduces complexity and increases reusability.  

    - **Inheritance**: Child classes can inherit properties and methods of parent class. It gets rid of redundant code. 

    - **Abstraction**: Abstraction allows the user to use the program easier. It hides unnecessary information and only shows what is important. It groups properties and methods of common purpose and name them. Interface becomes simpler and there is less chance of users to cause unwanted change to the code. It decreases complexity.

    - **Polymorphism**: Variables and functions of same names can be interpreted differently. It is also related to inheritance. When the parent class changes its properties or methods, the child classes can also use that changes. Use polymorphism to refactor ugly switch/case statements


  **Instantiation Pattern** (Method to create Object before Class keyword was created)

  1. ## **Functional**

     ![img](https://miro.medium.com/max/1028/1*SPZnQAWqfvZSCz4Y4rzyzg.png)

    
    **Advantage**: This is a method many people use to create a new object. All the functions are in an object so the code is easy to understand. Properties are in a closed scope, making them private.

    **Disadvantage**: All the methods in a function so when a second instance is created, all the methods and properties need to be copied. When this pattern is used to create a new object after some changes are made to the methods, each object will reference different methods in memory.

  
  2. ## **Functional Shared Instantiation**

     ![img](https://miro.medium.com/max/1053/1*H2EIw20YPMPz7weTmFcD9w.png)

    Functional shared pattern covers the disadvnatage of functional pattern. This pattern does not copy the methods when an instance is created so it improves memory management and efficiency. There is a different object that has all the methods, so the memory address of that object is only referenced. One disadvantage could be that when a new instance is created after the object that contains all the methods is edited, the new instance and the original each reference methods at different address.



3. ## **Prototypal Instantiation**

   ![img](https://miro.medium.com/max/1054/1*hyJgQk5ausq5kkQr4Ty_Ew.png)

   Prototypal pattern uses Object.create to create an object (like the title!). You need to connect the new object with the object with the methods using Object.create (refer to the diagram). Object.create will create an object that uses a specific object as prototype. 

   **Advantage**: Methods are connected to the prototype object and is not returned within the object. No methods need to be copied, so memory is used more efficiently. 

​   **Disadvantage**: To use this pattern, a separate object needs to be created and be filled with methods.



4. ## **Pseudoclassical**

![img](https://miro.medium.com/max/1053/1*65-jFc67sI1B5zRm_91vyQ.png)

    Pseudoclassical also uses a prototype like the prototypal pattern. Using a "new" keyword, a new instance is created. Instead of using Object.create, this pattern uses "this". The "this" keyword sets the properties and uses "new" keyword to create a new instance. It is one of the most common patterns to use, but it is harder to design the program to use this pattern. This pattern is great for code reusability.


Sources - https://medium.com/dailyjs/instantiation-patterns-in-javascript-8fdcf69e8f9b

# Conclusion

This post got a little longer than I thought it would be... In the next post, we will go over prototype in javascript!