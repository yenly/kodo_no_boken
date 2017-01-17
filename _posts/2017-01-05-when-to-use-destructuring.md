---
layout: post
title:  When To Use Destructuring
date:   2017-01-05 11:12:00 -0800
categories: ES6
---

Today I learned two clear examples of when to use destructuring.

### Example of why we destructure an object

When we need to pass a long argument list to a function. Instead of hardcoding the list, we should create an object with the arguments with properties. Then pass this object into the function and the function will destructure out the properties. The benefits are the list can grow dynamically and we do not need to know the order of the properties.

{% highlight javascript %}
const user = {
  username: 'myname',
  password: 'mypassword',
  email: 'myemail@example.com',
  dateOfBirth: '1/1/1980',
  city: 'New York'
}

function signup({ username, password, email, city, dateOfBirth }) {
  // create new user
}

signup(user);
{% endhighlight %}



### Example of why we destructure an array

When we need to process a long list of arrays in an array usually pulled in from API. We use map function to transform the embedded arrays to objects for more meaningful use.

{% highlight javascript %}
const points = [
  [4, 5],
  [10, 1],
  [0, 40]
];

points.map(pair => {
  const [ x, y ] = pair;
});
// OR destruct in arugment and return object
points.map(([ x, y]) => {
  // return { x: x, y: y };
  return { x, y }; // uses object literal to condense code more
});
{% endhighlight %}


[ES6 Code Examples](https://github.com/yenly/es6_javascript/blob/master/destructuring.js)
