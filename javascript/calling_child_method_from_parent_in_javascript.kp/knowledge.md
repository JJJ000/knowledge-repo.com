---
title: Invoke a child method from the parent
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: A parent class can call a child class`s method by using the `this` keyword.
---

**Contents**

[TOC]

### Using the Prototype Chain

The prototype chain allows us to access methods and properties of the parent object from the child object. This can be done by using the `__proto__` property of the child object to access the parent object.

For example:

```javascript
// Parent
function Parent() {
  this.name = 'Parent';
  this.sayName = function() {
  console.log(this.name);
  }
}

// Child
function Child() {
  this.name = 'Child';
}

// Set the prototype of the Child to the Parent
Child.prototype = new Parent();

// Call the sayName method of the Parent from the Child
var child = new Child();
child.sayName(); // Outputs 'Parent'
```

### Using the call() Method

The `call()` method allows us to invoke a method of an object in the context of another object. This can be used to call a parent method from a child object.

For example:

```javascript
// Parent
function Parent() {
  this.name = 'Parent';
  this.sayName = function() {
  console.log(this.name);
  }
}

// Child
function Child() {
  this.name = 'Child';
}

// Create an instance of the Parent
var parent = new Parent();

// Create an instance of the Child
var child = new Child();

// Call the sayName method of the Parent in the context of the Child
parent.sayName.call(child); // Outputs 'Child'
```

### Using the apply() Method

The `apply()` method is similar to the `call()` method, but it allows us to pass an array of arguments to the method being invoked. This can be used to call a parent method from a child object.

For example:

```javascript
// Parent
function Parent() {
  this.name = 'Parent';
  this.sayName = function(prefix) {
  console.log(prefix + ' ' + this.name);
  }
}

// Child
function Child() {
  this.name = 'Child';
}

// Create an instance of the Parent
var parent = new Parent();

// Create an instance of the Child
var child = new Child();

// Call the sayName method of the Parent in the context of the Child
parent.sayName.apply(child, ['Hello']); // Outputs 'Hello Child'
```
