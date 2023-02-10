---
title: Change JSON object properties to camelcase (starting with lowercase)
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: You can use a library like Lodash to convert object properties to camelCase.
---

**Contents**

[TOC]

### Using JSON.stringify

The easiest way to convert JSON Object properties to (lower first) camelCase is to use the `JSON.stringify()` function. This function takes a JavaScript object and returns a string containing the JSON representation of the object. The `JSON.stringify()` function has an optional parameter, `replacer`, which can be used to modify the output of the stringified JSON. By passing a function as the `replacer` parameter, you can specify how the output should be formatted.

### Using a Regular Expression

Another way to convert JSON Object properties to (lower first) camelCase is to use a regular expression. Regular expressions are powerful tools for manipulating text and can be used to search and replace text in a string. By using a regular expression with the `string.replace()` method, you can search for a pattern in a string and then replace it with a different pattern. For example, you could use a regular expression to search for all instances of `"_"` in a string, and then replace those instances with an empty string, thus removing the underscores and converting the string to (lower first) camelCase.

### Using a Library

There are also libraries available which can be used to convert JSON Object properties to (lower first) camelCase. These libraries provide functions which can be used to easily convert JSON objects to a desired format. For example, the `lodash` library provides a `_.camelCase()` function which can be used to convert any string to (lower first) camelCase.

### Using a Custom Function

Finally, you can also create a custom function to convert JSON Object properties to (lower first) camelCase. This custom function can be written to iterate over the properties of a JSON object and convert them to (lower first) camelCase. This approach requires more code and is more time consuming than the other methods, but it can be useful if you need to do more complex transformations on the JSON object.
