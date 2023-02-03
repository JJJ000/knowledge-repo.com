---
title: What is the syntax for finding a #hash in a url using javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: You can check for a #hash in a URL using JavaScript by accessing the window.location.hash property.
---

**Contents**

[TOC]

#### Using String Methods

You can use the `indexOf()` method to check if a `#` is present in a URL. `indexOf()` will return the index of the first occurrence of a specified character or substring in a given string. 

```javascript
let url = "www.example.com/#hash";

if (url.indexOf('#') > -1) {
  // The URL contains a #hash
}
```

#### Using Regular Expressions

You can also use regular expressions to check for the presence of a `#` in a URL. The following expression will return `true` if a `#` is present in the string:

```javascript
let url = "www.example.com/#hash";
let regex = /#/;

if (regex.test(url)) {
  // The URL contains a #hash
}
```
