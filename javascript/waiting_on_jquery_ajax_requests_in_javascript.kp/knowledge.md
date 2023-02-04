---
title: Wait until all jquery ajax requests have been completed?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use the jQuery.when() method to wait until all jQuery Ajax requests are done.
---

**Contents**

[TOC]

### Using jQuery

The `$.when()` method can be used to wait until all jQuery Ajax requests are done. This method takes one or more deferred objects (usually the result of an $.ajax() call) and executes a callback when all deferred objects have been resolved or rejected.

### Example

```javascript
$.when(
    $.ajax({
        url: 'example.com/request1',
        dataType: 'json'
    }),
    $.ajax({
        url: 'example.com/request2',
        dataType: 'json'
    }),
    $.ajax({
        url: 'example.com/request3',
        dataType: 'json'
    })
).then(function(data1, data2, data3) {
    // All requests are done
});
```

### Using Promises

If the requests are made using the Fetch API, you can use the `Promise.all()` method to wait until all requests are done. This method takes an array of promises and returns a single promise that resolves when all of the promises in the array have resolved.

### Example

```javascript
Promise.all([
    fetch('example.com/request1'),
    fetch('example.com/request2'),
    fetch('example.com/request3')
]).then(function(responses) {
    // All requests are done
});
```
