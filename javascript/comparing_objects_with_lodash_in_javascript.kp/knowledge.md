---
title: What is the process for performing a thorough comparison of two objects using lodash?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Using the \_.isEqual() method from Lodash, you can do a deep comparison between two objects.
---

**Contents**

[TOC]

###Step 1: Import Lodash

In order to use Lodash to compare two objects, you must first import the Lodash library into your project.

```js
import _ from 'lodash';
```

###Step 2: Use _.isEqual

Once Lodash is imported, you can use the _.isEqual() method to compare two objects. This method accepts two parameters, the two objects you want to compare. It will return true if the objects are deeply equal, and false if they are not.

```js
const obj1 = {
    a: 1,
    b: 2
};

const obj2 = {
    a: 1,
    b: 2
};

const isEqual = _.isEqual(obj1, obj2); // true
```

###Step 3: Use _.isMatch

If you need to compare two objects and check if they match a certain criteria, you can use the _.isMatch() method. This method accepts two parameters, the object you want to compare and the criteria you want to match. It will return true if the object matches the criteria, and false if it does not.

```js
const obj1 = {
    a: 1,
    b: 2
};

const criteria = {
    a: 1
};

const isMatch = _.isMatch(obj1, criteria); // true
```

###Step 4: Use _.isMatchWith

If you need to compare two objects and check if they match a certain criteria, but you need to use a custom comparison function, you can use the _.isMatchWith() method. This method accepts three parameters, the object you want to compare, the criteria you want to match, and a custom comparison function. It will return true if the object matches the criteria, and false if it does not.

```js
const obj1 = {
    a: 1,
    b: 2
};

const criteria = {
    a: 1
};

const customCompare = (objValue, srcValue) => {
    // custom comparison logic
};

const isMatch = _.isMatchWith(obj1, criteria, customCompare); // true
```
