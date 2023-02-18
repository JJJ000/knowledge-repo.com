---
title: What is the syntax for adding elements to an array using jquery?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-18 00:00:00
updated_at: 2023-02-18 00:00:00
tldr: Use the jQuery.push() method to add items to an array in JSON.
---

**Contents**

[TOC]

1. Create the Array 

Create the array that you want to add items to. This can be done by using the `[]` syntax in JavaScript. For example, to create an empty array named `myArray`:

```javascript
var myArray = [];
```

2. Add Items to the Array 

Once the array has been created, you can add items to the array using the `push()` method. This method takes in the item you want to add as an argument. For example, to add an item named `item1` to the `myArray` array:

```javascript
myArray.push('item1');
```

3. Convert to JSON

Once the array has been populated with the desired items, you can convert the array to JSON using the `JSON.stringify()` method. This method takes in the array as an argument and returns a JSON string. For example, to convert the `myArray` array to JSON:

```javascript
var myArrayJSON = JSON.stringify(myArray);
```

4. Output the JSON

The final step is to output the JSON string to the desired location. This can be done using the `console.log()` method, or using the desired output method. For example, to output the `myArrayJSON` JSON string to the console:

```javascript
console.log(myArrayJSON);
```
