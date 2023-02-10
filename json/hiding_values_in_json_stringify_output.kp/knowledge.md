---
title: Exclude certain values from the output of json.stringify()
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: You can use the replacer parameter of JSON.stringify() to filter out values to be hidden from the output.
---

**Contents**

[TOC]

**Section 1: Use the Replacer Parameter**

The replacer parameter of the JSON.stringify() method can be used to hide certain values in the output. This parameter takes in a function or an array of strings and numbers that serve as a filter for the output. The function will be called for each item in the object and it can be used to modify the value or to filter out the value. The array of strings and numbers will be used to filter out the keys whose names are not present in the array. 

**Section 2: Example**

For example, if we have the following object:

```
const obj = {
  name: 'John Doe',
  age: 25,
  address: '123 Main St'
};
```

We can use the replacer parameter to filter out the address from the output:

```
JSON.stringify(obj, ['name', 'age'])
```

The above code will return the following output:

```
{"name":"John Doe","age":25}
```

**Section 3: Use the Space Parameter**

The space parameter of the JSON.stringify() method can also be used to hide certain values in the output. This parameter takes in an integer or a string which specifies the number of spaces to use for indentation. If this parameter is set to 0, then the output will be compact and all values will be hidden. 

**Section 4: Example**

For example, if we have the following object:

```
const obj = {
  name: 'John Doe',
  age: 25,
  address: '123 Main St'
};
```

We can use the space parameter to hide the address from the output:

```
JSON.stringify(obj, 0)
```

The above code will return the following output:

```
{"name":"John Doe","age":25}
```
