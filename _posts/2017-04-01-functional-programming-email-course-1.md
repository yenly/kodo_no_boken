---
layout: post
title:  Functional Programming Email Course Notes
date:   2017-04-01 11:55:06 -0800
categories: JavaScript
tags: JavaScript FunctionalProgramming
---

Following are my notes to the first half of Functional Programming Email course by Preethi Kashireddy for future review.

### Functional Programming is a way of writing code.

Every software program has two things: behavior and data.
* Behavior is handled purely using functions. Functions are "self-contained" pieces of code that accomplish a specific task; defines relationship between set of possible inputs and outputs.
* Data is immutable (can't be changed). Functions in functional programming take in data as input and always produce new values as output. Functions can be passed around easily as data.

Break any complex problem down into smaller subproblems, solve them using functions, and finally combine them together to solve the bigger problem.

### Pure Functions

Two qualities to make a function "pure"
1. Function depends only on the input provided to it to produce a result (and not on any external state).
2. Function does not cause an observable side effects (i.e. modifying a global object or modifying a parameter passed by reference).

Benefits:
* Pure functions are predictable. Ideally, the only things a pure function needs to work properly are the arguments passed to it explicitly.
* Pure functions are easy to test.
* Deterministic and well-suited for parallel-processing.

Ultimate goal is not to eliminate side effects, but to confine them.

### Immutability

Immutable data means it's state cannot change after it's created. To create an immutable object, create a new object with the changed value and point your reference to it. In In JS, all primitive types (String, Number, Boolean, Null, Undefined, Symbol) are inherently immutable.

Objects are mutable. You can update, rewrite, erase over time. Ways to make objects immutable:
* Object.freeze
* [immutable.js](https://github.com/facebook/immutable-js){:target="_blank"}
* [seamless-immutable](https://github.com/rtfeldman/seamless-immutable){:target="_blank"}

Why does it matter?
* When you treat all data as fixed values, the concept of time goes away.
* No side effects. Functions can now be evaluated at any time and in any order. Results is guaranteed to always be the same.
* Makes values easy to share.
* Make it safer & easier to do concurrent programming.
* Avoid temporal coupling.
* Eliminate defensive copies.

### Referential Transparency

If a function consistently yields the same result for the same input, it is referentially transparent. Referential transparency gives us the ability to freely replace an express with its value and not change the behavior of the program.

**pure function + immutable data = referential Transparency**

Benefits
* Easier to refactor and rewrite programs
* Referential transparency implies that a function is pure. Let us focus on reactoring the single function without having to worry about all the outside world baggages.
* Helpful for optimizing code using memoization, common subexpression elimination, lazy evaluation, parallelization.

Helpful resources:
* [Learn the fundamentals of functional programming — for free, in your inbox](https://medium.freecodecamp.com/learning-the-fundamentals-of-functional-programming-425c9fd901c6){:target="_blank"}
