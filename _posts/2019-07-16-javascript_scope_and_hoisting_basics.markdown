---
layout: post
title:      "JavaScript: Scope and Hoisting Basics"
date:       2019-07-16 22:13:09 -0400
permalink:  javascript_scope_and_hoisting_basics
---


Lets talk about two fundamental building blocks of JavaScript: Scope and Hoisting. 

To start with the topic of scope, simply put, means the location in your code that a variable is declared. A variable is a name given to some data you wish to hold in memory. They are written as a declaration and initialization, typically. See below example:
```
var newVariable = "I'm a string that can be accessed later with this identifier called newVariable!"
     (declaration)                                               (initialization)
```

Anything outside of a function *but* inside a JS file( or between two script tags ) will be **globally** scoped. Any variable declared inside of a function will be **locally** scoped. Globally scoped declarations will be available for use anywhere in your code. The locals will only be available inside the function at hand. Lets look at a simple example:
```
var hey = "Hey!"  

function sayHey() {
 // LOCAL- inside this function
     var hi = "Hi!"
 console.log(hi) // Hi!
}

// GLOBAL- outside function
console.log(hey)
// Hey!
```

As of the release of ES6, we now have access to variables `const` and `let`. These have whats called **block** scope. Meaning their scope is available within the block in which they are defined. Blocks are usually anything between curly braces. Blocks are also created with `if`, `for`, and `while`loops. Block scope does not apply to `var`. Lets see an example:
```
 function animal() {
   if (true){
	    var cat = "Felix"
			let dog = "Pluto"
			const fish = "Nemo"
	 }
	 console.log(cat)
	 console.log(dog)
	 console.log(fish)
 }
 
 animal()
 //result:
 //Felix
 //dog is not defined  ---let is block scoped and only avaliable in the block
 //fish is not defined --- same goes for const
```
Last thing on scope: **Lexical** scope. This means the children functions inside of a parent function have access to the context of the parent. Lets take the above example and refactor it a little bit:
 ```
 function mamaAnimal() {
	  var cat = "Felix"
  	let dog = "Pluto"
		const fish = "Nemo"
		
       function babyAnimal() {
      	 console.log(cat)
	       console.log(dog)
	      console.log(fish)
	 }
	 babyAnimal()	 
 }
 
 mamaAnimal()
 //result:
 //Felix
//Pluto
//Nemo
```
Now that we understand scope a bit better, we can go over hoisting. Lets first understand that when a document is loaded, the JavaScript is read in two phases. The first phase is the creation phase- a lot of stuff happens here but as it relates to hoisting- the variable and function declarations made throughout your code are read and set aside in memory. The second phase is called the execution phase and that is where assigments are made. Lets circle back around to the first example given at the very top:
 ```
var newVariable = "I'm a string that can be accessed later with this identifier called newVariable!"
  (declaration- this variable name **only** is stored in memory)       (assigment is executed in 2nd phase)
```

Now on to how this relates to hoisting. Hoisting means that variable and function declarations are moved to the top of their scope, regardless of if that scope is global or local. Hoisting **does not** apply to `let` or `const`. To help this sink in lets look at an example:
```
function sayHey(greeting){
    console.log(greeting)
}

sayHey("What's Up?")
//What's Up?
```

But lets take this out of the traditional order and see what happens:
```
sayHey("What's Up?")

function sayHey(greeting){
    console.log(greeting)
}
//What's Up?
```
**This** is hoisting. Because our function declaration was saved to memory in the compile phase, we can access and invoke it in this order. However there are many ways, especially when writing declarations using `var` that bugs can happen so best practices would tell you to always declare a variable at the top of ther respective scope:
```
//BAD EXAMPLE:
console.log(a)
var a = "A"
// undefined

//GOOD EXAMPLE:
var a = "A"
console.log(a)
//A
```

These are the beginning concepts in understanding hoist and scope. They are in no way all of what you need to know about each subject but are a great starting point to help you with understanding the two. Happy coding and thanks for reading!

