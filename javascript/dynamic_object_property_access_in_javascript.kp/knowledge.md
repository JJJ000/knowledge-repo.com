---
title: Retrieving an object attribute using a name that is calculated at runtime
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: You can use bracket notation to access an object property with a dynamically-computed name in Javascript.
---

**Contents**

[TOC]

### Dot Notation

Dot notation is the most common way to access an object property with a dynamically-computed name in Javascript. This is done by using the bracket notation syntax, where the name of the property is computed as a string inside the brackets. 

For example, if we have an object `person` with the properties `name` and `age`, we can access the `name` property with a dynamically-computed name like this: 

```javascript
let propName = 'name';
let personName = person[propName];
```

### Bracket Notation

Bracket notation is another way to access an object property with a dynamically-computed name in Javascript. This is done by using the dot notation syntax, where the name of the property is computed as a string inside the brackets. 

For example, if we have an object `person` with the properties `name` and `age`, we can access the `name` property with a dynamically-computed name like this: 

```javascript
let propName = 'name';
let personName = person.propName;
```

### Object.keys()

The `Object.keys()` method can also be used to access an object property with a dynamically-computed name in Javascript. This method returns an array of the object's enumerable property names. 

For example, if we have an object `person` with the properties `name` and `age`, we can access the `name` property with a dynamically-computed name like this: 

```javascript
let propName = 'name';
let personName = Object.keys(person).find(key => key === propName);
```

### Object.getOwnPropertyNames()

The `Object.getOwnPropertyNames()` method can also be used to access an object property with a dynamically-computed name in Javascript. This method returns an array of all the object's own property names. 

For example, if we have an object `person` with the properties `name` and `age`, we can access the `name` property with a dynamically-computed name like this: 

```javascript
let propName = 'name';
let personName = Object.getOwnPropertyNames(person).find(key => key === propName);
```
