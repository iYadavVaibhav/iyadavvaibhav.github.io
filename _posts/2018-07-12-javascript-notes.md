---
layout: post
title: JavaScript Notes
categories: notes, javascript
---

Notes on JavaScript as I learn and improve my understanding.

## Functions Concepts

Functions can do whatever we want them to do.. :)

**How Functions behave:**

We can make a function in JS by defining it like we define a variable.

```javascript
myFunction = function(arg1, arg2, arg3) {
  // all that you want to do
  // use args or may be they are optional
  //...
  return myResult;
}
```

now this function can return a variable which could possibly be any data/object/json etc.

**Using this function**

Function can now be used to get the result

```javascript
myFunction(arg1, arg2).done( function (data) {
  // Now do what you want to do with result in data
});
```

Now we see that, done would be triggered once myFunction is completed. All jQuery promises provide a done method that takes a callback.

## JS Objects Concept

JS Object can hold anything, they can even hold another function.
They are accessed using . DOT notation.