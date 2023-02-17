---
title: What is the syntax to transform a JSON object into a key=value format using jq?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: jq can be used to convert a JSON object to key=value format using the -r option.
---

**Contents**

[TOC]

**Section 1: Using the jq Command**

1. Navigate to the directory containing the JSON file.
2. Run the command `jq -r 'to_entries[] | "\(.key)=\(.value)"' < filename.json`

**Section 2: Understanding the Command**

The command `jq -r 'to_entries[] | "\(.key)=\(.value)"'` is used to convert a JSON object to key=value format. The `to_entries` function is used to convert the JSON object into an array of key-value pairs. The `[]` operator is then used to iterate through each element of the array. The `.key` and `.value` functions are used to access the key and value of each element respectively. The `\(.key)` and `\(.value)` are used to interpolate the values into the string. Finally, the `-r` flag is used to output the result in raw strings.  

**Section 3: Example**

For example, consider the following JSON object:

```
{
    "name": "John",
    "age": 30
}
```

Running the command `jq -r 'to_entries[] | "\(.key)=\(.value)"' < filename.json` will output the following:

```
name=John
age=30
```

**Section 4: Conclusion**

In conclusion, the jq command can be used to convert a JSON object to key=value format. The `to_entries` function is used to convert the JSON object into an array of key-value pairs. The `[]` operator is then used to iterate through each element of the array. The `.key` and `.value` functions are used to access the key and value of each element respectively. The `\(.key)` and `\(.value)` are used to interpolate the values into the string. Finally, the `-r` flag is used to output the result in raw strings.
