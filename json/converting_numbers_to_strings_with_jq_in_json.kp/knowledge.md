---
title: What is the syntax for using jq to turn a number into a string?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use the `.tostring` function to convert a number to a string in JSON using jq.
---

**Contents**

[TOC]

### Using the `tostring()` Method

The `tostring()` method of jq can be used to convert a number to a string. This method takes the number as an argument and returns a string.

For example, to convert the number `123` to a string, you can use the following jq command:

```
jq '. | tostring(123)'
```

The output will be a string representation of the number `123`.

### Using the `tonumber()` Method

The `tonumber()` method of jq can also be used to convert a number to a string. This method takes the number as an argument and returns a string representation of the number.

For example, to convert the number `123` to a string, you can use the following jq command:

```
jq '. | tonumber(123)'
```

The output will be a string representation of the number `123`.

### Using the `format()` Method

The `format()` method of jq can also be used to convert a number to a string. This method takes two arguments: the number to be converted, and a string containing the format to be used for the conversion.

For example, to convert the number `123` to a string, you can use the following jq command:

```
jq '. | format("%s", 123)'
```

The output will be a string representation of the number `123`.

### Using the `@text` Filter

The `@text` filter of jq can also be used to convert a number to a string. This filter takes the number as an argument and returns a string representation of the number.

For example, to convert the number `123` to a string, you can use the following jq command:

```
jq '. | @text(123)'
```

The output will be a string representation of the number `123`.
