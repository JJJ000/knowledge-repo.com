---
title: What is the best way to show a JavaScript object?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: You can display a JavaScript object by using the console.log() method.
---

**Contents**

[TOC]

### Using console.log()

The simplest way to display a JavaScript object is to use the `console.log()` function. This function takes in any number of arguments, and will print out the values of those arguments in the console. For example, if you have an object `myObject` with the following properties:

```js
const myObject = {
  name: 'John',
  age: 30,
  city: 'New York'
};
```

You can display the object in the console by calling `console.log(myObject);`:

```js
console.log(myObject);
```

This will output the following in the console:

```
{ name: 'John', age: 30, city: 'New York' }
```

### Using JSON.stringify()

Another way to display a JavaScript object is to use the `JSON.stringify()` function. This function takes in an object as an argument and returns a stringified version of the object. For example, if you have an object `myObject` with the same properties as above, you can use `JSON.stringify()` to display it in the console:

```js
console.log(JSON.stringify(myObject));
```

This will output the following in the console:

```
{"name":"John","age":30,"city":"New York"}
```

### Using for...in loop

You can also use a `for...in` loop to display a JavaScript object. This loop iterates over the properties of an object and prints out the name and value of each property. For example, if you have an object `myObject` with the same properties as above, you can use a `for...in` loop to display it in the console:

```js
for (const key in myObject) {
  console.log(`${key}: ${myObject[key]}`);
}
```

This will output the following in the console:

```
name: John
age: 30
city: New York
```

### Using Object.entries()

Finally, you can use the `Object.entries()` function to display a JavaScript object. This function takes in an object as an argument and returns an array of key-value pairs. For example, if you have an object `myObject` with the same properties as above, you can use `Object.entries()` to display it in the console:

```js
console.log(Object.entries(myObject));
```

This will output the following in the console:

```
[ ["name", "John"], ["age", 30], ["city", "New York"] ]
```
