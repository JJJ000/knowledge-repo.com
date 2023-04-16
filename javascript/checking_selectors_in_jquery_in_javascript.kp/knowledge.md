---
title: What is the process for testing if a jquery selector is targeting an element?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can use the jQuery .is() method to check if a selector matches something in jQuery.
---

**Contents**

[TOC]

**Using the .is() Method:**

1. Create a jQuery object with the selector you want to test.

```javascript
var selector = $('.my-selector');
```

2. Use the .is() method to test if the selector matches something.

```javascript
if (selector.is(':visible')) {
  // do something
}
```

**Using the .length Property:**

1. Create a jQuery object with the selector you want to test.

```javascript
var selector = $('.my-selector');
```

2. Check the length of the jQuery object.

```javascript
if (selector.length > 0) {
  // do something
}
```
