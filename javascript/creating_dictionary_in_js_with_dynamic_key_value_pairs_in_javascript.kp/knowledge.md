---
title: How can I dynamically add key-value pairs to a dictionary in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: You can create a dictionary and add key value pairs dynamically in Javascript using the bracket notation.
---

**Contents**

[TOC]

#### Section 1: Creating a Dictionary
In JavaScript, a dictionary is represented as an object. To create a dictionary, you can use the object literal notation.

```javascript
var myDictionary = {};
```

#### Section 2: Adding Key-Value Pairs
To add a key-value pair to a dictionary, you can use the following syntax:

```javascript
myDictionary[key] = value;
```

Where `key` is the key you want to add, and `value` is the value you want to assign to that key.

#### Section 3: Adding Multiple Key-Value Pairs
You can add multiple key-value pairs to a dictionary by using a loop. For example, if you have an array of key-value pairs, you can use `forEach` to iterate over that array and add each pair to the dictionary.

```javascript
var keyValuePairs = [
    ["key1", "value1"],
    ["key2", "value2"],
    ["key3", "value3"]
];

keyValuePairs.forEach(function(pair) {
    myDictionary[pair[0]] = pair[1];
});
```

#### Section 4: Adding Key-Value Pairs Dynamically
If you want to add key-value pairs to a dictionary dynamically, you can use a loop and prompt the user for input.

```javascript
var myDictionary = {};

while (true) {
    var key = prompt("Please enter a key:");
    var value = prompt("Please enter a value:");

    myDictionary[key] = value;
}
```

In this example, the loop will continue until the user cancels the prompt.
