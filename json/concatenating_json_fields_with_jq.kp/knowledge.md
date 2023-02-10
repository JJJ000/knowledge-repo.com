---
title: Combine two values in a JSON object using jq
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: jq can be used to concatenate two fields in JSON by using the `+.\` operator.
---

**Contents**

[TOC]

**Section 1: Overview**

The jq command line utility can be used to concatenate two fields in a JSON object. This allows you to combine two fields into a single value. This can be useful when you need to combine two values into a single value for further processing or manipulation.

**Section 2: Syntax**

The syntax for concatenating two fields in a JSON object using jq is as follows:

`.field1 + .field2`

**Section 3: Example**

For example, given the following JSON object:

```
{
  "name": "John",
  "age": 30
}
```

You can use jq to concatenate the two fields as follows:

`jq '.name + .age'`

This will return the value "John30".

**Section 4: Conclusion**

Using the jq command line utility, you can easily concatenate two fields in a JSON object. This can be useful when you need to combine two values into a single value for further processing or manipulation.
