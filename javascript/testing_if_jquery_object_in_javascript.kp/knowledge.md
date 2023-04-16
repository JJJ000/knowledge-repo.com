---
title: Verify if the object is a jquery object
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can check if an object is a jQuery object by using the jQuery.isPlainObject() method.
---

**Contents**

[TOC]

#### Using jQuery's is() Function

The jQuery is() function can be used to check if an object is a jQuery object. It takes a parameter, which can be a selector expression or an element, and returns true if the object is a jQuery object.

```javascript
if ($(selector).is()) {
    // jQuery object
} else {
    // not a jQuery object
}
```

#### Using the instanceof Operator

The instanceof operator can be used to check if an object is a jQuery object. It takes two parameters - an object and a constructor - and returns true if the object is an instance of the given constructor.

```javascript
if (object instanceof jQuery) {
    // jQuery object
} else {
    // not a jQuery object
}
```

#### Checking the jQuery Prototype

The jQuery prototype can be used to check if an object is a jQuery object. It takes a parameter - the object to check - and returns true if the object is a jQuery object.

```javascript
if (jQuery.prototype.isPrototypeOf(object)) {
    // jQuery object
} else {
    // not a jQuery object
}
```

#### Checking the jQuery Constructor

The jQuery constructor can also be used to check if an object is a jQuery object. It takes a parameter - the object to check - and returns true if the object is a jQuery object.

```javascript
if (object.constructor === jQuery) {
    // jQuery object
} else {
    // not a jQuery object
}
```
