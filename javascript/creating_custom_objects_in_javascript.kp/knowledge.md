---
title: What is the correct way to create a custom object in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Create a custom object in JavaScript by assigning properties and values to an object literal or by using the Object constructor.
---

**Contents**

[TOC]

### Step 1: Define the Object

The first step in creating a custom object in JavaScript is to define the object. This can be done by assigning an object literal to a variable. For example:

```javascript
var myObject = {};
```

### Step 2: Add Properties and Methods

Once the object has been defined, properties and methods can be added by using dot notation or bracket notation. For example:

```javascript
myObject.name = "John";
myObject["age"] = 25;
myObject.sayHello = function() {
    console.log("Hello!");
};
```

### Step 3: Use the Object

Once the object has been defined and properties and methods have been added, the object can be used by calling its methods and accessing its properties. For example:

```javascript
myObject.sayHello(); // prints "Hello!"
console.log(myObject.name); // prints "John"
```

### Step 4: Modify the Object

Finally, the object can be modified by adding, removing, or changing its properties and methods. For example:

```javascript
myObject.name = "Jane";
myObject.sayGoodbye = function() {
    console.log("Goodbye!");
};
delete myObject.age;
```
