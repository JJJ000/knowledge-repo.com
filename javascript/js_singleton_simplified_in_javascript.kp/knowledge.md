---
title: The most straightforward and efficient way to create a singleton in javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: The simplest way to implement a singleton in JavaScript is to create an object literal and assign it to a variable.
---

**Contents**

[TOC]

**Section 1: Definition**

A singleton is a design pattern that restricts the instantiation of a class to one "single" instance. This is useful when exactly one object is needed to coordinate actions across the system.

**Section 2: Implementation**

The simplest way to implement a singleton in JavaScript is to use the module pattern. This pattern involves creating an immediately-invoked function expression (IIFE) that returns an object literal containing the methods and properties of the singleton. The IIFE ensures that the singleton is instantiated only once.

```
const Singleton = (function () {
  let instance;

  function init() {
    // Private methods and variables
    function privateMethod() {
      console.log('I am private');
    }

    let privateVariable = 'Im also private';

    return {
      // Public methods and variables
      publicMethod: function () {
        console.log('The public can see me!');
      },

      publicProperty: 'I am also public',

      getPrivateVariable: function () {
        return privateVariable;
      }
    };
  };

  return {
    getInstance: function () {
      if (!instance) {
        instance = init();
      }

      return instance;
    }
  };
})();
```

**Section 3: Usage**

The singleton can be used by calling the `getInstance()` method of the `Singleton` object. This will return the same instance every time, ensuring that only one instance of the singleton is ever created.

```
const instance1 = Singleton.getInstance();
const instance2 = Singleton.getInstance();

console.log(instance1 === instance2); // true
```

**Section 4: Benefits**

Using the singleton pattern has several benefits, including:

- Ensures that only one instance of the class is ever created
- Allows for global access to the single instance
- Makes it easier to manage and coordinate shared resources across the application
