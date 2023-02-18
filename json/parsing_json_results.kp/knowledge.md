---
title: Learn how to extract data from JSON and access the results
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-18 00:00:00
updated_at: 2023-02-18 00:00:00
tldr: To parse JSON and access results, use a JSON library to deserialize the JSON data into a data structure (e.g. a dictionary) and then use the keys to access the values.
---

**Contents**

[TOC]

## Parsing JSON

JSON (JavaScript Object Notation) is a lightweight data-interchange format. It is easy for humans to read and write, and it is easy for machines to parse and generate. JSON can be parsed using language-specific libraries, such as JavaScript's `JSON.parse()` function.

## Accessing Results

Once the JSON data has been parsed, the data can be accessed using the dot operator (`.`) or the bracket operator (`[]`). The dot operator is used to access the value of a key, while the bracket operator is used to access the value of an array index.

For example, if the parsed JSON object contains a key `name` with a value of `John`, then the value can be accessed using the dot operator, like this:

```js
var name = parsedJSONObject.name; // name will be "John"
```

If the parsed JSON object contains an array of names, then the value of the first item in the array can be accessed using the bracket operator, like this:

```js
var firstName = parsedJSONObject.names[0]; // firstName will be "John"
```

## Iterating Over Results

If the parsed JSON object contains an array of objects, then the values of each object can be accessed by iterating over the array. For example, if the parsed JSON object contains an array of `person` objects, then the values of each `person` object can be accessed by looping over the array, like this:

```js
for (var i = 0; i < parsedJSONObject.people.length; i++) {
  var person = parsedJSONObject.people[i];
  console.log(person.name); // will log the name of each person
}
```

## Conclusion

JSON is a lightweight data-interchange format that is easy to parse and access. Once the JSON data has been parsed, the data can be accessed using the dot operator (`.`) or the bracket operator (`[]`). If the parsed JSON object contains an array of objects, then the values of each object can be accessed by iterating over the array.
