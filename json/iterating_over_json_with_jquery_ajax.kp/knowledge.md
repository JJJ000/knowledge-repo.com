---
title: How can I iterate through the JSON data returned from an ajax call using jquery?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: jQuery`s $.each() function can be used to loop over JSON data returned from an AJAX success call.
---

**Contents**

[TOC]

### Section 1: Accessing the Data

In order to access the data, you must first retrieve it from the AJAX call. This can be done using the `$.ajax()` method.

```javascript
$.ajax({
  type: 'GET',
  url: 'url/to/json/file',
  success: function(data) {
    // code to access the data
  }
});
```

### Section 2: Parsing the Data

Once the data is retrieved, it must be parsed in order to access it. This can be done using the `$.parseJSON()` method.

```javascript
var data = $.parseJSON(data);
```

### Section 3: Looping Through the Data

Once the data is parsed, it can be looped through using the `$.each()` method.

```javascript
$.each(data, function(index, value) {
  // code to loop through the data
});
```

### Section 4: Accessing the Values

Within the loop, the values can be accessed using the `value` parameter.

```javascript
$.each(data, function(index, value) {
  console.log(value);
});
```
