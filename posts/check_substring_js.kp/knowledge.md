---
title: What is the method for determining if a string includes a specific substring in JavaScript?
authors:
- cool_wizard
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-01-02 00:00:00
updated_at: 2023-01-02 00:00:00
tldr: Use either `includes()` or `indexOf()` of the `String` object.
---

**Contents**

[TOC]

### Using the include() method

In JavaScript, you can use the `includes()` method of the `String` object to check if a string contains a particular substring.

Here's an example of how you can use the includes() method:

```JS
let string = 'Hello, world!';

if (string.includes('Hello')) {
  console.log('The string includes the substring "Hello"');
} else {
  console.log('The string does not include the substring "Hello"');
}
```

This will print `The string includes the substring "Hello"` to the console.

### Using the indexOf() method

You can also use the `indexOf()` method of the `String` object to check if a string contains a particular substring. This method returns the index of the first occurrence of the substring within the string, or `-1` if the substring is not found.

Here's an example of how you can use the `indexOf()` method:

```JS
let string = 'Hello, world!';

if (string.indexOf('Hello') !== -1) {
  console.log('The string includes the substring "Hello"');
} else {
  console.log('The string does not include the substring "Hello"');
}
```

This will also print `The string includes the substring "Hello"` to the console.
