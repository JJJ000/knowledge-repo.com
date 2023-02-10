---
title: Extracting data from an xmlhttprequest response in JSON format
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: You can parse the JSON from an XmlHttpRequest.responseJSON object by using the JSON.parse() method.
---

**Contents**

[TOC]

## Section 1: Parsing JSON

Parsing JSON is the process of converting a JSON string into a JavaScript object. This is done using the `JSON.parse()` method. This method takes a string as an argument and returns the parsed object.

## Section 2: XmlHttpRequest.responseJSON

XmlHttpRequest.responseJSON is a JavaScript object that contains the response from an XMLHttpRequest. This object is usually returned from an AJAX call and contains the data returned from the server.

## Section 3: Using JSON.parse()

In order to parse the data from the XmlHttpRequest.responseJSON object, the JSON.parse() method can be used. This method takes the response object as an argument and returns the parsed object.

## Section 4: Example

For example, if the response object contains the following JSON string:

```
{
    "name": "John Doe",
    "age": 30
}
```

Then the following code can be used to parse the data:

```
var responseObj = XmlHttpRequest.responseJSON;
var parsedObj = JSON.parse(responseObj);
```

The parsedObj variable now contains the parsed object with the name and age properties.
