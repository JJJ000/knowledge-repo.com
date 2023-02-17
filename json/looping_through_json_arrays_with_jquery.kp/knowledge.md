---
title: Iterate through a JSON array using jquery and retrieve each key/value pair
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: Use the jQuery each() method to iterate through the JSON array and get the key/value pair.
---

**Contents**

[TOC]

## Section 1: Parsing the JSON

In order to loop and get key/value pairs from a JSON array using jQuery, the JSON must first be parsed. This can be done by using the `$.parseJSON()` method. The syntax for this method is as follows:

```js
var json_object = $.parseJSON(json_string);
```

Where `json_string` is a string representation of the JSON array.

## Section 2: Looping Through the Array

Once the JSON array has been parsed, it can be looped through using the `$.each()` method. The syntax for this method is as follows:

```js
$.each(json_object, function(key, value){
    // code to execute for each key/value pair
});
```

Where `json_object` is the parsed JSON array, `key` is the key name, and `value` is the corresponding value.

## Section 3: Accessing the Key/Value Pairs

Within the `$.each()` function, the key and value of each pair can be accessed. For example:

```js
$.each(json_object, function(key, value){
    console.log("Key: " + key);
    console.log("Value: " + value);
});
```

This code will log the key and value of each key/value pair in the console.

## Section 4: Example

Here is a full example of looping through a JSON array and logging the key/value pairs to the console:

```js
// parse the JSON array
var json_object = $.parseJSON('[{"name": "John", "age": 30}, {"name": "Jane", "age": 25}]');

// loop through the array
$.each(json_object, function(key, value){
    console.log("Key: " + key);
    console.log("Value: " + value);
});
```

This code will log the following to the console:

```
Key: 0
Value: Object {name: "John", age: 30}
Key: 1
Value: Object {name: "Jane", age: 25}
```
