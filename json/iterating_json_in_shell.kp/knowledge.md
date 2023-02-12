---
title: Looping over a JSON array in a shell script
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: One can iterate through a JSON array in a Shell script by using a loop to read each element of the array.
---

**Contents**

[TOC]

# Section 1: Parsing JSON

The most common way to parse a JSON array in a Shell script is to use a command-line JSON processor such as `jq`. `jq` is a lightweight and flexible command-line JSON processor that can be used to parse, filter, and transform JSON data.

# Section 2: Using jq

To use `jq` to iterate through a JSON array, you first need to pipe the JSON data into `jq`. This can be done using the `cat` command. 

Once the JSON data is piped into `jq`, you can use the `.` operator to iterate through the array. The `.` operator will iterate through each element in the array and will return the value of each element.

# Section 3: Example

For example, if you have the following JSON array:

```json
[
  "foo",
  "bar",
  "baz"
]
```

You can use `jq` to iterate through the array and print each element as follows:

```bash
cat array.json | jq -r '.[]'
```

This will print the following output:

```
foo
bar
baz
```

# Section 4: Conclusion

In conclusion, `jq` is a powerful command-line JSON processor that can be used to parse, filter, and transform JSON data. It can also be used to iterate through a JSON array and print each element.
