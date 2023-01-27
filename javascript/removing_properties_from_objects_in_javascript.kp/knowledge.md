---
title: What is the best way to delete a property from a JavaScript object?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: Use the delete operator to remove a property from a JavaScript object.
---

**Contents**

[TOC]

**1. Using the Delete Operator**

The delete operator can be used to remove a property from a JavaScript object. The syntax is as follows:

```javascript
delete objectName.propertyName;
```

Where `objectName` is the name of the object and `propertyName` is the name of the property you want to delete.

**2. Using the Object.defineProperty() Method**

The Object.defineProperty() method can also be used to remove a property from a JavaScript object. The syntax is as follows:

```javascript
Object.defineProperty(objectName, propertyName, {
    configurable: false
});
```

Where `objectName` is the name of the object and `propertyName` is the name of the property you want to delete.

**3. Using the Object.defineProperties() Method**

The Object.defineProperties() method can also be used to remove a property from a JavaScript object. The syntax is as follows:

```javascript
Object.defineProperties(objectName, {
    [propertyName]: {
        configurable: false
    }
});
```

Where `objectName` is the name of the object and `propertyName` is the name of the property you want to delete.

**4. Using the Object.assign() Method**

The Object.assign() method can also be used to remove a property from a JavaScript object. The syntax is as follows:

```javascript
Object.assign(objectName, {
    [propertyName]: undefined
});
```

Where `objectName` is the name of the object and `propertyName` is the name of the property you want to delete.
