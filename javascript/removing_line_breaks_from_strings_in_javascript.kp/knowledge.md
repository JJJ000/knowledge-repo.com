---
title: What is the best way to get rid of all line breaks in a string?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use the replace() method to replace all line breaks with an empty string.
---

**Contents**

[TOC]

### Using Regular Expressions

Using regular expressions, you can remove all line breaks from a string with the following code:

```javascript
var str = "This is a\nstring\nwith\nline\nbreaks";
str = str.replace(/\r?\n|\r/g, "");
```

### Using a Loop

You can also use a loop to remove all line breaks from a string:

```javascript
var str = "This is a\nstring\nwith\nline\nbreaks";
var newStr = "";
for (var i = 0; i < str.length; i++) {
    if (str.charAt(i) !== "\n") {
        newStr += str.charAt(i);
    }
}
```

### Using the Split Method

You can also use the `split()` method to remove all line breaks from a string:

```javascript
var str = "This is a\nstring\nwith\nline\nbreaks";
var newStr = str.split("\n").join("");
```

### Using the Replace Method

Finally, you can use the `replace()` method to remove all line breaks from a string:

```javascript
var str = "This is a\nstring\nwith\nline\nbreaks";
var newStr = str.replace(/\n/g, "");
```
