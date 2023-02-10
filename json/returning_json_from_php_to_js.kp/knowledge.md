---
title: Retrieving JSON data from a PHP script in javascript
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: PHP can return JSON data to JavaScript by using the json\_encode() function.
---

**Contents**

[TOC]

### Section 1: Using PHP to Generate JSON

PHP can be used to generate JSON objects to be used in JavaScript applications. To generate a JSON object in PHP, you can use the `json_encode()` function. This function takes in a PHP array as an argument and returns a JSON object.

For example, the following code will generate a JSON object from an array of data:

```php
$data = array(
  'name' => 'John',
  'age' => 30,
  'city' => 'New York'
);

$json = json_encode($data);
```

### Section 2: Accessing JSON in JavaScript

Once the JSON object has been generated, it can be accessed in JavaScript using the `JSON.parse()` method. This method takes in a JSON string as an argument and returns a JavaScript object.

For example, the following code will access the JSON object generated in the previous section:

```js
var json = JSON.parse(json);
console.log(json.name); // Outputs 'John'
```

### Section 3: Using AJAX to Request JSON

In addition to generating JSON in PHP, it is also possible to request JSON objects from a server using AJAX. This can be done using the `XMLHttpRequest` object in JavaScript.

For example, the following code will make an AJAX request to a server and return a JSON object:

```js
var xhr = new XMLHttpRequest();
xhr.open('GET', 'https://example.com/data.json', true);
xhr.onload = function() {
  if (this.status == 200) {
    var json = JSON.parse(this.responseText);
    console.log(json);
  }
};
xhr.send();
```

### Section 4: Using jQuery to Request JSON

Another popular way to request JSON from a server is to use the jQuery library. jQuery provides a `$.getJSON()` method which can be used to request JSON data from a server.

For example, the following code will make an AJAX request to a server and return a JSON object:

```js
$.getJSON('https://example.com/data.json', function(json) {
  console.log(json);
});
```
