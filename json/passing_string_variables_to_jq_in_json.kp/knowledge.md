---
title: Is it possible to provide a string variable to jq instead of a file?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: Yes, you can pass a string variable to jq by using the -n flag.
---

**Contents**

[TOC]

**Section 1: Introduction**

Yes, it is possible to pass a string variable to jq. jq is a lightweight and flexible command-line JSON processor that is used to parse, filter, and transform JSON data. It is designed to work with both structured and unstructured data, allowing developers to quickly and easily manipulate and extract data from JSON documents.

**Section 2: How to Pass a String Variable to jq**

The simplest way to pass a string variable to jq is to use the `--arg` flag, which allows developers to specify a name and value for a variable. This flag can be used to pass a string variable to jq, which can then be used within the jq program.

**Section 3: Example**

Let's say we have a string variable called `my_string` with a value of `hello world`. To pass this variable to jq, we can use the `--arg` flag like this:

```
jq --arg my_string "hello world"
```

This will pass the variable `my_string` with a value of `hello world` to jq. We can then use the variable in our jq program, for example:

```
jq --arg my_string "hello world" '.my_string'
```

This will return the value of the `my_string` variable, which is `hello world`.

**Section 4: Conclusion**

In conclusion, it is possible to pass a string variable to jq using the `--arg` flag. This allows developers to quickly and easily manipulate and extract data from JSON documents.
