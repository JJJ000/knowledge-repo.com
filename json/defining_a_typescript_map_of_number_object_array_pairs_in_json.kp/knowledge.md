---
title: What is the syntax for creating a typescript map that has a number as the key and an array of objects as the value?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-16 00:00:00
updated_at: 2023-02-16 00:00:00
tldr: A Typescript Map of key-value pairs can be defined as a Map<number, object[]> where the key is a number and the value is an array of objects in JSON format.
---

**Contents**

[TOC]

### Section 1: Defining the Map

A Typescript Map of key value pairs, where the key is a number and the value is an array of objects in JSON, can be defined as follows:

```typescript
const myMap: Map<number, object[]> = new Map();
```

### Section 2: Adding Entries

Entries can be added to the Map by using the `set()` method:

```typescript
myMap.set(1, [{name: 'John', age: 20}, {name: 'Jane', age: 25}]);
myMap.set(2, [{name: 'Bob', age: 30}, {name: 'Alice', age: 35}]);
```

### Section 3: Retrieving Entries

Entries can be retrieved from the Map by using the `get()` method:

```typescript
const entry1 = myMap.get(1); // returns [{name: 'John', age: 20}, {name: 'Jane', age: 25}]
const entry2 = myMap.get(2); // returns [{name: 'Bob', age: 30}, {name: 'Alice', age: 35}]
```

### Section 4: Iterating Through Entries

Entries can be iterated through by using the `forEach()` method:

```typescript
myMap.forEach((value, key) => {
    console.log(`Key: ${key}, Value: ${JSON.stringify(value)}`);
});
```

This will output the following:

```
Key: 1, Value: [{"name":"John","age":20},{"name":"Jane","age":25}]
Key: 2, Value: [{"name":"Bob","age":30},{"name":"Alice","age":35}]
```
