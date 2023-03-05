---
title: To set a variable object key in react, one can utilize immutability-helper
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: You can use the `$set` command in immutability-helper to set a variable object key in a JSON object in React.
---

**Contents**

[TOC]

## Introduction to Immutability-helper in React

Immutability-helper is a utility library for React and React Native that allows developers to create immutable update structures in a more concise and readable way. It provides several helper functions that can be used to update data while maintaining a state that is immutable.

## Setting a Variable Object Key in JSON using Immutability-helper

In React, it is common to work with JSON data that contains objects with variable keys. Sometimes the key of an object is not known until runtime or depends on some other conditions. To set a variable object key in JSON using immutability-helper, we can use the `$merge` helper function.

```
import update from 'immutability-helper';

const data = {
  header: {
    title: 'Hello World',
  },
};

const variableKey = 'body';

const newData = update(data, {
  [variableKey]: {
    $merge: {
      text: 'Lorem Ipsum',
    },
  },
});

console.log(newData);
```

In the above example, we have a `data` object that contains a `header` object. We want to add a new object to the `data` object with the variable key `body`. We use the `$merge` helper function to merge the new object into the existing object at the variable key.

## Using `$set` to Set a Variable Object Key in JSON

Another way to set a variable object key in JSON using immutability-helper is to use the `$set` helper function. This function allows us to set the value of an object property to a new value.

```
import update from 'immutability-helper';

const data = {
  header: {
    title: 'Hello World',
  },
};

const variableKey = 'body';

const newData = update(data, {
  [variableKey]: {
    $set: {
      text: 'Lorem Ipsum',
    },
  },
});

console.log(newData);
```

In this example, we use the `$set` helper function to set the value of the property at the variable key to a new object with a `text` property.

## Conclusion

In conclusion, immutability-helper is a useful library for updating data in a more concise and readable way in React applications. It provides several helper functions like `$merge` and `$set` that can be used to update data while maintaining immutability. By using these helper functions, we can easily set variable object keys in JSON data.
