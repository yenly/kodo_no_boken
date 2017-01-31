---
layout: post
title:  ES6 Generators
date:   2017-01-30 4:55:00 -0800
categories: ES6
---

Today I learned generators are functions we can enter and exit multiple times. They work perfectly with for-of-loop especially when we want to iterate through objects with any type of data structure. We can use Symbol.iterator is a tool that teaches the objects how to respond to for-of-loop. With it, we can have multiple generators working together. A great practical example would be using Symbol.iterator to recursively iterate over a tree data structure to access each node.

[ES6 Code Examples](https://github.com/yenly/es6_javascript/blob/master/generators.js) 
