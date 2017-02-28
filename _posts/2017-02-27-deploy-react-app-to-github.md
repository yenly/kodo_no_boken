---
layout: post
title:  React App on Github Pages
date:   2017-02-27 11:47:00 -0800
categories: React
tags: React, Github
---

I read an article on [How to Deploy my Create React App to Github pages](https://medium.freecodecamp.com/surge-vs-github-pages-deploying-a-create-react-app-project-c0ecbf317089#.yqp0poieb) and thought I have to try this. So much possibilities! Today I practiced build and deploy on my first [Create React App](https://github.com/facebookincubator/create-react-app), [Stopwatch](https://github.com/yenly/react_stopwatch), made from a workshop in October 2016. Lessons learned:
* Always cross reference the instructions from the article to the docs/guides provided by Create React App repo.
* React eco-system changes so fast that the deploy method in the article is different than the Create React App I've used to bootstrap. Hence, build and deploy yielded a blank page because it could not find the CSS and JS files even though they are checked in on my Github.
* I bootstrapped a new react app and copied over the code from the old repo. Stepped through the build and deploy steps and magically [Stopwatch](https://yenly.github.io/stopwatch/) is up and running!

Helpful resources:
* [Surge VS GitHub Pages: How to deploy a create-react-app project](https://medium.freecodecamp.com/surge-vs-github-pages-deploying-a-create-react-app-project-c0ecbf317089#.yqp0poieb)
* [Create React App Doc - Deploy to Github Page](https://github.com/yenly/stopwatch#github-pages)
