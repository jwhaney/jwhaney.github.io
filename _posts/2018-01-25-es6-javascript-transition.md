---
layout: post
title: What is ES6 and why should I use it?
date: 2018-01-25 10:41
author: john
categories: web
location: austin
description: I have recently started learning the fairly new modern ES6 JavaScript standard (actually, ES7 is making it's way as we speak but let's hold our horses on that). I had read about it before, but had not actually used it and didn't understand why I would need it.
---
I have recently started learning the fairly new modern ES6 JavaScript standard (actually, ES7 is making way as we speak but hold your horses on that). I had read about it before, but had not actually used it and did not understand why I would need it. There are so many new things that I have to learn already, why do I need to learn new things about the language itself? Why change the language? Turns out there is some good reason, of course.

[ECMAScript 6 (ES6)](http://es6-features.org) is the new version of JavaScript which introduces some new things that every developer should start taking advantage of. Below I have bulleted out some of the most important additions from my perspective:

* **Constants**

  You can define an immutable number in your code which will stay the same over time. You will get an error if you try to overwrite that constant later with something else.

  ```javascript
  const imaJsConstant = 2424
  ```

* **Let**

  let is the new var. Using let is the new way to define variables in your code that you can change later. When you define a variable with let, it is [scoped](https://www.w3schools.com/js/js_scope.asp) to the exact block of code it is inside, not globally.

  ```javascript
  let imaJsLetNumber = 48
  let imaJsLetString = 'let string'
  ```

* **Arrow Functions**

  A pretty big change or addition to the language in ES6 is that you can declare a function using `=>` instead of `function test(){...}`, so you can declare a const function that does not change throughout your code like this:

  ```javascript
  const testFunc = (arg1) => arg1
  ```

* **Modules**

  I have read that developers have used modules for quite some time now, but it has never been native until now. ES6 modules are stored in separate files with the .js file extension, and only one module can be in a file. The most important thing here is that modules can help you clean up your code nicely, and break it down into chunks that are more easily maintained. Here is a simple example:

  *testModule.js*
  ```javascript
  function randomNum(){
    return Math.random();
  }

  function sum(a,b) {
    return a + b;
  }

  export {randomNum, sum}
  ```
  *app.js*
  ```javascript
  import { randomNum, sum } from 'testModule';

  console.log(randomNum()); //console logs a random number
  console.log(sum(44, 100)); //console logs sum output 144
  ```

* **Classes**

  JavaScript has classes now, like pretty much every other object-oriented programming language. ES6 classes bring support for inheritance, constructors, static methods, etc. I am actually not really well versed in classes, yet, but I understand the value and how they encourage interoperability, etc. Check out the link below for a good example of ES6 classes:

  [https://github.com/lukehoban/es6features#classes](https://github.com/lukehoban/es6features#classes)


There are a lot of other changes/additions that are important so I would definitely read up on them. I have some references below where I found some good info. It seems like the most popular browsers (Chrome, Firefox, Edge, Safari) fully support ES6, so make the move already!

#### References:

  [6 reasons Web developers need to learn JavaScript ES6 now](https://thenextweb.com/dd/2016/03/09/6-reasons-need-learn-javascript-es6-now-not-later/)

  [GitHub user @lukehoban es6features repo](https://github.com/lukehoban/es6features)

  [MDN web docs - Arrow functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions)

  [Understanding ES6 Modules](https://www.sitepoint.com/understanding-es6-modules/)
