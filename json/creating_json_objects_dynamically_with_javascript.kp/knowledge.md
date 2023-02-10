---
title: Generate a JSON object dynamically using JavaScript (without string concatenation)
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: You can create a JSON object dynamically via JavaScript by using the JSON.stringify() method.
---

**Contents**

[TOC]

**Section 1: Creating the Object**

We can create a JavaScript object without concatenating strings by simply assigning values to object properties. For example, the following code creates an object with three properties, each with its own value:

```javascript
let myObject = {
  name: 'John',
  age: 30,
  job: 'Engineer'
};
```

**Section 2: Adding Properties**

We can also add properties to an existing object using the dot notation or bracket notation. For example, the following code adds a new property to the myObject object:

```javascript
myObject.hobby = 'Running';
```

**Section 3: Removing Properties**

We can also remove properties from an existing object using the delete keyword. For example, the following code removes the hobby property from the myObject object:

```javascript
delete myObject.hobby;
```

**Section 4: Accessing Properties**

We can also access the properties of an object using the dot notation or bracket notation. For example, the following code accesses the name property of the myObject object:

```javascript
let name = myObject.name; // 'John'
```
