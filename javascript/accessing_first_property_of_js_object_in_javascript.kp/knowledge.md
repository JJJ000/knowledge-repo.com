---
title: What is the syntax for accessing the first property of a JavaScript object?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: The first property of a Javascript object can be accessed using dot notation or bracket notation.
---

**Contents**

[TOC]

# Accessing the First Property of a JavaScript Object

## 1. Defining the Object

The first step to accessing the first property of a JavaScript object is to define the object itself. This can be done by using the `let` or `const` keyword to declare the object and setting it equal to a set of key-value pairs. 

```javascript
let person = {
  name: 'John',
  age: 25,
  location: 'New York'
};
```

## 2. Accessing the Property

Once the object is declared, the first property of the object can be accessed using dot notation or bracket notation. 

### Dot Notation

Dot notation allows you to access the value of a property by specifying the property name after a period. In the example above, the first property of the `person` object is `name`. To access this property using dot notation, you can use the following syntax:

```javascript
person.name
```

### Bracket Notation

Bracket notation allows you to access the value of a property by specifying the property name inside of square brackets. In the example above, the first property of the `person` object is `name`. To access this property using bracket notation, you can use the following syntax:

```javascript
person['name']
```

## 3. Outputting the Value

Once the property is accessed, you can output the value of the property to the console or store it in a variable for later use. To output the value of the `name` property using `console.log()`, you can use the following syntax:

```javascript
console.log(person.name)
// Outputs 'John'
```

## 4. Storing the Value

You can also store the value of the property in a variable for later use. To store the value of the `name` property in a variable called `name`, you can use the following syntax:

```javascript
let name = person.name;
console.log(name);
// Outputs 'John'
```
