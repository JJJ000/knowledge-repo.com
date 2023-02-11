---
title: What is the best way to filter JSON data using JavaScript or jquery?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: You can filter JSON Data in JavaScript or jQuery by using the .filter() method.
---

**Contents**

[TOC]

#### Section 1: Using JavaScript

To filter JSON data in JavaScript, you can use the `filter()` method. This method takes a callback function as an argument and returns a new array containing all the elements that pass the test implemented by the callback function.

For example, to filter an array of JSON objects by a given key, you can use the following code:

```javascript
const jsonData = [{
  "name": "John",
  "age": 25
}, {
  "name": "Jane",
  "age": 30
}, {
  "name": "Joe",
  "age": 28
}];

const filteredData = jsonData.filter(item => item.age > 25);

console.log(filteredData);
// [{
//   "name": "Jane",
//   "age": 30
// }, {
//   "name": "Joe",
//   "age": 28
// }]
```

#### Section 2: Using jQuery

To filter JSON data in jQuery, you can use the `grep()` method. This method takes a callback function as an argument and returns a new array containing all the elements that pass the test implemented by the callback function.

For example, to filter an array of JSON objects by a given key, you can use the following code:

```javascript
const jsonData = [{
  "name": "John",
  "age": 25
}, {
  "name": "Jane",
  "age": 30
}, {
  "name": "Joe",
  "age": 28
}];

const filteredData = $.grep(jsonData, item => item.age > 25);

console.log(filteredData);
// [{
//   "name": "Jane",
//   "age": 30
// }, {
//   "name": "Joe",
//   "age": 28
// }]
```

#### Section 3: Using Lodash

To filter JSON data in Lodash, you can use the `filter()` method. This method takes a callback function as an argument and returns a new array containing all the elements that pass the test implemented by the callback function.

For example, to filter an array of JSON objects by a given key, you can use the following code:

```javascript
const jsonData = [{
  "name": "John",
  "age": 25
}, {
  "name": "Jane",
  "age": 30
}, {
  "name": "Joe",
  "age": 28
}];

const filteredData = _.filter(jsonData, item => item.age > 25);

console.log(filteredData);
// [{
//   "name": "Jane",
//   "age": 30
// }, {
//   "name": "Joe",
//   "age": 28
// }]
```

#### Section 4: Using Ramda

To filter JSON data in Ramda, you can use the `filter()` method. This method takes a callback function as an argument and returns a new array containing all the elements that pass the test implemented by the callback function.

For example, to filter an array of JSON objects by a given key, you can use the following code:

```javascript
const jsonData = [{
  "name": "John",
  "age": 25
}, {
  "name": "Jane",
  "age": 30
}, {
  "name": "Joe",
  "age": 28
}];

const filteredData = R.filter(item => item.age > 25, jsonData);

console.log(filteredData);
// [{
//   "name": "Jane",
//   "age": 30
// }, {
//   "name": "Joe",
//   "age": 28
// }]
```
