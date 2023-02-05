---
title: What is the best way to get the hostname from a url in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: The hostname portion of a URL can be extracted using the `location.hostname` property of the window object.
---

**Contents**

[TOC]

### 1. Using the URL Object

The URL object is a built-in JavaScript object which provides properties and methods for working with URLs. To extract the hostname from a URL, you can use the `hostname` property of the URL object.

```javascript
let url = new URL('http://www.example.com/path/to/page');
let hostname = url.hostname;
// hostname = 'www.example.com'
```

### 2. Using Regular Expressions

Regular expressions are a powerful tool for matching patterns in strings. You can use a regular expression to extract the hostname from a URL.

```javascript
let url = 'http://www.example.com/path/to/page';
let hostname = url.match(/^(?:https?:\/\/)?(?:[^@\n]+@)?(?:www\.)?([^:\/\n]+)/im)[1];
// hostname = 'www.example.com'
```

### 3. Using String Manipulation

You can also extract the hostname from a URL using string manipulation.

```javascript
let url = 'http://www.example.com/path/to/page';
let hostname = url.split('/')[2];
// hostname = 'www.example.com'
```

### 4. Using the Location Object

If you are working with a web page, you can also use the `location` object to extract the hostname.

```javascript
let hostname = location.hostname;
// hostname = 'www.example.com'
```
