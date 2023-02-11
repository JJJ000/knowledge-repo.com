---
title: How can I determine if a 'key' exists in jq before looping through its values?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: You can use the `has` function to check for the presence of a key in a JSON object before iterating over its values.
---

**Contents**

[TOC]

### Option 1: Using the `has()` Function

The `has()` function can be used to check if a key is present in a JSON object before iterating over the values. To use the `has()` function, simply pass the key as an argument to the function.

For example, if we want to check if the key `name` is present in the following JSON object:

```
{
  "name": "John",
  "age": 25
}
```

We can use the `has()` function as follows:

```
if (has("name")) {
  // Do something here
}
```

### Option 2: Using the `keys()` Function

The `keys()` function can also be used to check if a key is present in a JSON object before iterating over the values. To use the `keys()` function, simply pass the key as an argument to the function.

For example, if we want to check if the key `name` is present in the following JSON object:

```
{
  "name": "John",
  "age": 25
}
```

We can use the `keys()` function as follows:

```
if (keys("name")) {
  // Do something here
}
```

### Option 3: Using the `in` Operator

The `in` operator can also be used to check if a key is present in a JSON object before iterating over the values. To use the `in` operator, simply pass the key as an argument to the operator.

For example, if we want to check if the key `name` is present in the following JSON object:

```
{
  "name": "John",
  "age": 25
}
```

We can use the `in` operator as follows:

```
if ("name" in . ) {
  // Do something here
}
```

### Option 4: Using the `test()` Function

The `test()` function can also be used to check if a key is present in a JSON object before iterating over the values. To use the `test()` function, simply pass the key as an argument to the function.

For example, if we want to check if the key `name` is present in the following JSON object:

```
{
  "name": "John",
  "age": 25
}
```

We can use the `test()` function as follows:

```
if (test("name")) {
  // Do something here
}
```
