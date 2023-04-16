---
title: How to delete an element from a JavaScript object
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the delete operator to remove an item from a JavaScript object.
---

**Contents**

[TOC]

**Option 1: Using delete Operator**

1. Declare the object to delete the item from.

```javascript
let myObj = {
  item1: 'value1',
  item2: 'value2',
  item3: 'value3'
};
```

2. Use the delete operator to delete the item from the object.

```javascript
delete myObj.item2;
```

3. The object now looks like this:

```javascript
let myObj = {
  item1: 'value1',
  item3: 'value3'
};
```

**Option 2: Using Object.assign()**

1. Declare the object to delete the item from.

```javascript
let myObj = {
  item1: 'value1',
  item2: 'value2',
  item3: 'value3'
};
```

2. Create a new object without the item to delete.

```javascript
let newObj = Object.assign({}, myObj);
delete newObj.item2;
```

3. Assign the new object to the original object.

```javascript
myObj = newObj;
```

4. The object now looks like this:

```javascript
let myObj = {
  item1: 'value1',
  item3: 'value3'
};
```
