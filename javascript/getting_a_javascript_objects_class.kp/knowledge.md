---
title: What is the class of a JavaScript object?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: The class of a JavaScript object can be retrieved using the Object.prototype.toString() method.
---

**Contents**

[TOC]

# Section 1: Overview

JavaScript objects do not have a "class" property, so it is not possible to get an object's class in the same way as other programming languages. However, there are some workarounds that can be used to determine an object's class.

# Section 2: Using the Constructor Property

One way to determine an object's class is to use the constructor property. This property is set to the function that was used to create the object. For example, if you create an object using the `new` keyword, the constructor property will be set to the constructor function.

For example:

```javascript
function Person(name, age) {
  this.name = name;
  this.age = age;
}

var person = new Person("John", 30);

console.log(person.constructor); // Person(name, age)
```

# Section 3: Using the instanceof Operator

Another way to determine an object's class is to use the `instanceof` operator. This operator checks if an object is an instance of a particular constructor function.

For example:

```javascript
function Person(name, age) {
  this.name = name;
  this.age = age;
}

var person = new Person("John", 30);

console.log(person instanceof Person); // true
```

# Section 4: Using the Object.prototype.toString() Method

The `Object.prototype.toString()` method can be used to get the string representation of an object. This method will return a string containing the object's class.

For example:

```javascript
function Person(name, age) {
  this.name = name;
  this.age = age;
}

var person = new Person("John", 30);

console.log(Object.prototype.toString.call(person)); // [object Object]
```
