---
layout: post
title: JavaScript Libraries and Frameworks Notes
categories: notes javascript
last_modified_at: 2019-08-01 12:53:18
---

## Node JS
Overview:
- node js is like asp/php/flask
- you can run .js files outside browser
- give ability to use js in backend
- npm is package manager like pip for node js
- pakages are nothing but js libraries.

## Angular JS
Overview:
- We can define a resource in app folder eg: hero.ts to include the class with it's members.
- We can make components for various behaviors of our app. eg: 
  - heroes - to list all heroes
  - hero-detail - to keep functionality for one hero

## Typescript
It is superset of javascript, basically used to make use of new features of JS coming with ES6, ES7 and compile them back to old ES3 that can be used with IE and Safari as well.

## JavaScript
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

Function can now be used to get the result

```javascript
myFunction(arg1, arg2).done( function (data) {
  // Now do what you want to do with result in data
});
```

Now we see that, done would be triggered once myFunction is completed. All jQuery promises provide a done method that takes a callback.

**JS Objects Concept**
- JS Object can hold anything, they can even hold another function.
- They are accessed using . DOT notation.

**Related Posts:**
- [NativeScript](../nativescript-notes)