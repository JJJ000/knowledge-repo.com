---
title: Retrieve the property names of a typescript interface as an array of strings
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Use Object.keys() to get an array of strings of the keys of a Typescript interface in Javascript.
---

**Contents**

[TOC]

### Step 1: Retrieve the Keys of the Interface

In order to retrieve the keys of a Typescript interface, we can use the `Object.keys()` method. This method takes an object as an argument and returns an array of strings representing the object's enumerable properties. 

```javascript
const interfaceObj = {
  name: 'John',
  age: 30
};

const keys = Object.keys(interfaceObj);
// keys = ['name', 'age']
```

### Step 2: Convert the Keys to Strings

The `Object.keys()` method returns an array of strings representing the object's enumerable properties. However, if the interface contains any non-string values, they will need to be converted to strings before they can be used.

This can be done using the `String()` method, which takes any value as an argument and returns a string representation of that value.

```javascript
const interfaceObj = {
  name: 'John',
  age: 30
};

const keys = Object.keys(interfaceObj);
const stringKeys = keys.map(key => String(key));
// stringKeys = ['name', 'age']
```

### Step 3: Return the Array of Strings

Once the keys have been converted to strings, we can return the array of strings.

```javascript
const interfaceObj = {
  name: 'John',
  age: 30
};

const keys = Object.keys(interfaceObj);
const stringKeys = keys.map(key => String(key));
return stringKeys;
// returns ['name', 'age']
```

### Step 4: Use the Function

Finally, we can use the function to retrieve the keys of a Typescript interface as an array of strings.

```javascript
const getInterfaceKeysAsStrings = (interfaceObj) => {
  const keys = Object.keys(interfaceObj);
  const stringKeys = keys.map(key => String(key));
  return stringKeys;
};

const interfaceObj = {
  name: 'John',
  age: 30
};

const keys = getInterfaceKeysAsStrings(interfaceObj);
// keys = ['name', 'age']
```
