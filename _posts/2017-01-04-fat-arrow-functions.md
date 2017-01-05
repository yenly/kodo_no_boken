---
layout: post
title:  Fat Arrow Functions
date:   2017-01-04 5:12:00 -0800
categories: ES6
---

Today I learned fat arrow functions make use of "lexical this." It makes value of "this" behave as we expect it to. This is a better solution than using bind.

Rules of fat arrow functions:
<ol>
  <li>If the function has a single expression in its body, the curly braces and 'return' keyword can be removed.</li>
  <li>If the function has a single argument, the parentheses around the argument list can be removed.</li>
</ol>

[ES6 Code Examples]: https://github.com/yenly/es6_javascript/blob/master/fat_arrow_functions.js
