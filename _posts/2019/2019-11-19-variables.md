---
title: Variables in Javascript
date: 2019-11-19 10:31:30
categories:
- Javascript
tags: Basic Review Variable
---

# Variable
The first topic of the review is variable. 

There are two ways to assign and pass on variables. The first is to copy the value and the second is to copy the reference(address) and pass it on.

You can copy the variable to a memory of fixed size or the address of its memory by the Type of variable.


## Type #1

The first type to go over is Primitive Type, which is also called Scalar or Simple Type. 
Primitive Type copies the value.


- Null

- Undefined

- Boolean

- String

- Number

## Type #2

The second type to go over is Reference Type, which refers to the memory address. Also called Container or Complex Type.

- Array

- Object

- Function


Let's try this out. 

```js
// Example #1)

let a = "Hey I'm Joshua";

function trick (input) {

  input = "Hey I'm David"
  
}
console.log(trick(a));
```

What is the value of a in this case?

For Primitive Type, the original does not change. Only the copied value changes. Therefore, the value of a is: "Hey I'm Joshua". 

```js
// Example #2)

let a = {name: "Joshua"}

function trick(input){

  input.name = "David"

}

console.log(trick(a));
```

When you copy Reference Type, the original value changes because the value at that memory address changes. 
a will be "David". 

# TL;DR

In summary, 

For **Primitive Type (null, undefined, string, number, Boolean)**, the original value does not change even after it goes through a function. 

For **Reference Type (Array, Object, Function)**, the original value changes because the memory address is copied.

Remember!