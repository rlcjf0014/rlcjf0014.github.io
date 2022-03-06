---
title: Function Method (call, apply, bind)
date: 2022-03-03 11:31:30
categories:
- Javascript
tags: Basic Review Function 
---

# Introduction
Today's post will be about methods to call functions, which are .call, .apply and .bind. 
The difference between .call and .apply is the way you receive parameter. 

.call receives paramter one by one while .apply receives it as an array. 

# Call & Apply
 Let's check out some examples of **call** and **apply**.
 

```js
function add (x, y){

  this.val = x+y;

  console.log(this.val)
}



let obj = {val: 0};



add.call(obj, 2, 8); //10

add.apply(obj, [2, 8]); //10

```
Both call and apply carry out functions, but the parameters are passed in differently. 


```js

let arr = [1, 4, 2, 8, 3];

Math.max.apply(null, arr); //8
```

When apply receives an array and "this" does not mean anything, put in null.


# .bind

.bind does not carry out function like call or apply. It returns the function that "this" is binded to.


```js

let bindit = add.bind(obj, 2, 8); 
```

When bindit is called, the add function binds obj as this and calls the function. 
It only calls and does not execute like closure. 
Therefore, **bindit** will give you a result of 10. bind is usually used to bind the value of "this" to something.


```js

function whatisprice (allowance, cost){
  this.cost = cost;
  this.allowance = allowance;



  this.getchange = function () {
    return this.allowance - this.cost;
  }
  
  this.printchange = function () {
    console.log(this.getchange() )
  }

};



let water = new whatisprice(50, 20);
water.printchange() //30;

```
The code above shows that "this" is water, which is an instance of the class whatisprice. 


## When do we use this?

When do we use bind?

```js
setTimeout(water.printchange, 5000); 
```

When the code above is called, can 30 be printed after 5 seconds? The answer is no. 

When setTimeout is called, the value of this is window. 
Therefore, since water is not "this", an error will appear. To solve this, we use bind to set the value of this as water.
 

```js

setTimeout(water.printchange.bind(water), 5000); 
```

When we bind the value of this as water, the code works!


## Currying 

Currying is also possible with bind! 

```js

function greeting (name, age) {
  return "Hi, my name is " + name + " and I am " + age;
}



let Joshua = greeting.bind(null, "Joshua");

```

The code above (Joshua) returns the function greeting. However, "Joshua" is binded inside that function. 
Since the value of "this" was not set, the first parameter of bind is null.


```js

Joshua(25); // Returns "Hi, my name is Joshua and I am 25"

```

**Remember! bind is used to set the value of "this"**