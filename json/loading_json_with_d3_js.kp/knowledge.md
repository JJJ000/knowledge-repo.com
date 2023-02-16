---
title: Loading JSON data into d3.js without a http get request
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-15 00:00:00
updated_at: 2023-02-15 00:00:00
tldr: Yes, d3.js can load JSON data without a HTTP GET request using the d3.json() method.
---

**Contents**

[TOC]

#### Loading JSON from a File

The most straightforward way to load JSON data into d3.js is from a file. To do this, you'll need to use the d3.json() method. This method is used to asynchronously load a JSON file and then execute a callback function once the file is loaded. The callback function is passed two arguments, an error object (if an error occurred) and the parsed JSON data.

For example:

```
d3.json("data.json", function(error, data) {
  if (error) throw error;
  // do something with the data
});
```

#### Loading JSON from an API

If you need to load JSON data from an API, you can use the d3.json() method as well. The only difference is that you'll need to specify the API URL instead of a file path.

For example:

```
d3.json("https://api.example.com/data", function(error, data) {
  if (error) throw error;
  // do something with the data
});
```

#### Loading JSON from a String

If you already have a JSON string, you can use the d3.json() method to parse it into an object. To do this, you'll need to pass the string as the first argument, and then specify a callback function as the second argument.

For example:

```
var jsonString = '{"foo": "bar"}';
d3.json(jsonString, function(error, data) {
  if (error) throw error;
  // do something with the data
});
```

#### Loading JSON from an Object

If you already have a JavaScript object, you can use the d3.json() method to parse it into a JSON string. To do this, you'll need to pass the object as the first argument, and then specify a callback function as the second argument.

For example:

```
var myObject = {foo: "bar"};
d3.json(myObject, function(error, data) {
  if (error) throw error;
  // do something with the data
});
```
