---
title: Scope & Hoisting in Javascript
date: 2022-01-29 11:31:30
categories:
- Javascript
tags: Basic Review Scope Hoisting
---

# Introduction
Today's topic of review will be scope and hoisting. Score is a concept that you get used to while using var, let and const. It is very important to be well aware of this in Javascript. 

# Definition

Scope in javascript defines whether a variable can be accessed. There are two types of scope, which are **Global Scope** and **Local Scope**. In local scope, it is possible to access outer variable and function but it's impossible to access variable and function in local scope. Global scope is the scope at the highest order. In addition, scope can be present within a different scope. 

# Explanation

- Based on my search, javascript has supported function scope from before and not block scope. However, it started to support block scope from ES6.   

- Javascript originally has scope by function. Variables that were defined using var and functions declared by function declaration have function scope. From ES6, let and const are more often used to define variables and it became possible to distinguish scope by block. 

- **let** is block scope. You can reassign values, but cannot redefine the variable. 
- **const** is block scope. You cannot reassign or redefine with const. 
- **var** is function scope. You can reassign values and redefine the variable. It is not as widely used as before because function scope can cause confusion. 

_window is an object that covers globally. Therefore, function declared in global scope and variables that are defined with var are connect to window._


# How?

- There are two ways to determine a function's scope at a higher level. The first is by where the function was called and the second is where the function was declared. 

- The first way is called dynamic scope and the second is called either lexical and static scope. Javascript follows lexical scope, meaning that a function's scope is determined by where the function was declared, not where it was called. 

# Hoisting

While studying scope, I came accross hoisiting, which is one of the important concepts in Javascript. 

## Definition
- **Hoisting** by definition means to lift up, and can be interpreted as lifting up the declared variable or function to the highest level of code. 
- According to MDN, the declaration of variable or funciton is saved in memory in compilation stage, but is located where the code is written at. 
- Javascript compiles the code before reading it. It divides one code into two to read. Javascript reads **var a = 3;** as var and a = 3, dividing the declaring and assigning into two. It hoists the declaring part to the highest scope.


## Example
```js
Example)

function whatisheight() {

  console.log("My height is "+height)
  var height = 176;
  console.log("My height is "+height)

}


//Result:

//My height is undefined

//My height is 176
```

The first console log brings only the **var height** part due to hoisiting and will not cause error even when **var height = 176** occurs after. However, since the assignment is not hoisted, it prints undefined. The second console log correctly prints 176. 

One cool thing is that Javascript differentiates the declaring and assigning, so hoisiting is only valid for function declaration. 
If you create a function using function declaration, it is acknowledged as a variable, not a function after hoisting. 

Function declaration overrides variable declaration after hoisiting, 

```js

var food; //string

function food() {
  console.log("chicken");
}

console.log(typeof food); //function
```

When a value is assigned to the variable, the variable overrides the function declaration.

```js

var food = "pizza"; //string

function food() {
  console.log("chicken");
}

console.log(typeof food); //string

```

# Conclusion

**Variable Declaration + Assignment > Function Declaration > Variable Declaration;**

Scope and Hoisting Review finished!