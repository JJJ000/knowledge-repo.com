---
title: Include additional, changing key-value pairs in a JavaScript array or hash table
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: You can add dynamic key, value pairs to a JavaScript array or hash table in JSON by using the dot notation or square bracket notation.
---

**Contents**

[TOC]

### Adding New Key-Value Pairs to an Array

Adding new key-value pairs to an array is a simple process. All that needs to be done is to create a new array element with the desired key-value pair.

For example, if we wanted to add a new key-value pair with the key "name" and the value "John", we would do the following:

```javascript
var myArray = [
    {
        "key1": "value1"
    },
    {
        "key2": "value2"
    }
];

// Add new key-value pair
myArray.push({"name": "John"});
```

### Adding New Key-Value Pairs to a Hash Table

Adding new key-value pairs to a hash table in JSON is a bit more involved than adding them to an array. This is because the key-value pairs must be stored in a specific format that allows for efficient lookups.

The following is an example of how to store a new key-value pair in a hash table:

```javascript
var myHashTable = {
    "key1": "value1",
    "key2": "value2"
};

// Add new key-value pair
myHashTable["name"] = "John";
```

### Conclusion

Adding new key-value pairs to an array or hash table in JSON is a straightforward process. For arrays, all that needs to be done is to create a new array element with the desired key-value pair. For hash tables, the key-value pair must be stored in a specific format in order to allow for efficient lookups.
