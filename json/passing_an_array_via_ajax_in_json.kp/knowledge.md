---
title: Send an array as part of a $.ajax() request
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Pass the array as a JSON encoded string in the data option of the $.ajax() call.
---

**Contents**

[TOC]

### Using jQuery

1. Create the array in JavaScript:

```javascript
var myArray = [1,2,3];
```

2. Stringify the array into a JSON string:

```javascript
var myArrayJson = JSON.stringify(myArray);
```

3. Pass the JSON string as the data parameter in the $.ajax() call:

```javascript
$.ajax({
    url: 'someurl.php',
    type: 'POST',
    data: myArrayJson,
    success: function(data) {
        // do something with the data
    }
});
```

### Using Plain JavaScript

1. Create the array in JavaScript:

```javascript
var myArray = [1,2,3];
```

2. Stringify the array into a JSON string:

```javascript
var myArrayJson = JSON.stringify(myArray);
```

3. Create a new XMLHttpRequest object and set the content type to application/json:

```javascript
var xhr = new XMLHttpRequest();
xhr.setRequestHeader('Content-Type', 'application/json');
```

4. Pass the JSON string as the data parameter in the request:

```javascript
xhr.send(myArrayJson);
```
