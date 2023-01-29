---
title: Instantiating an object using the class name and invoking the constructor
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: To create an instance using the class name and calling constructor in Java, use the syntax `ClassName instanceName = new ClassName();`.
---

**Contents**

[TOC]

### Definition of a Constructor
A constructor is a special type of method that is used to initialize an object when it is created. Constructors are usually defined with the same name as the class they are used to create.

### Creating an Instance
To create an instance of a class, you must first create a variable of the class type, and then use the `new` keyword to create an instance of the class.

### Calling the Constructor
Once an instance of a class is created, the constructor can be called to initialize the object. The constructor can be called by using the variable name followed by parentheses.

### Example
For example, to create an instance of the `Person` class and call its constructor, the following code could be used:

```
Person person = new Person();
```
