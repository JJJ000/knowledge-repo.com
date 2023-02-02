---
title: Search for an item with a specific id in an array of JavaScript objects
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Use the Array.prototype.find() method to find an object by its id in an array of JavaScript objects.
---

**Contents**

[TOC]

### 1. Create an Array of Objects

```javascript
let people = [
  {
    id: 1,
    name: "John"
  },
  {
    id: 2,
    name: "Sally"
  },
  {
    id: 3,
    name: "Bob"
  }
  ];
```

### 2. Use Array.find()

```javascript
let person = people.find(person => person.id === 2);
console.log(person.name); // Sally
```

### 3. Use Array.filter()

```javascript
let person = people.filter(person => person.id === 2)[0];
console.log(person.name); // Sally
```

### 4. Use a For Loop

```javascript
let person;
for (let i = 0; i < people.length; i++) {
  if (people[i].id === 2) {
    person = people[i];
    break;
  }
}
console.log(person.name); // Sally
```
