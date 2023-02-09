---
title: Iterate over a JSON array using javascript
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: The best way to loop through a JSON array is to use a for loop.
---

**Contents**

[TOC]

**Section 1: For Loop**

The most common way to loop through an array of JSON objects is to use a for loop. This will iterate through each object in the array and allow us to access the properties of each object.

```javascript
var jsonArray = [{name: "John", age: 20}, {name: "Jane", age: 22}];

for (var i = 0; i < jsonArray.length; i++) {
  console.log(jsonArray[i].name);
  console.log(jsonArray[i].age);
}
```

**Section 2: For-in Loop**

Another way to loop through an array of JSON objects is to use a for-in loop. This will iterate through each object in the array and allow us to access the properties of each object.

```javascript
var jsonArray = [{name: "John", age: 20}, {name: "Jane", age: 22}];

for (var key in jsonArray) {
  console.log(jsonArray[key].name);
  console.log(jsonArray[key].age);
}
```

**Section 3: For-of Loop**

A third way to loop through an array of JSON objects is to use a for-of loop. This will iterate through each object in the array and allow us to access the properties of each object.

```javascript
var jsonArray = [{name: "John", age: 20}, {name: "Jane", age: 22}];

for (let obj of jsonArray) {
  console.log(obj.name);
  console.log(obj.age);
}
```

**Section 4: Array.forEach() Method**

The last way to loop through an array of JSON objects is to use the Array.forEach() method. This will iterate through each object in the array and allow us to access the properties of each object.

```javascript
var jsonArray = [{name: "John", age: 20}, {name: "Jane", age: 22}];

jsonArray.forEach(function(obj) {
  console.log(obj.name);
  console.log(obj.age);
});
```
