---
title: Omit column from jq JSON output
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: Use the `-c` option to exclude columns from the jq JSON output.
---

**Contents**

[TOC]

**Section 1: jq**

jq is a command-line JSON processor. It is used to parse, filter, and transform JSON data. It can be used to extract data from a JSON object, and to manipulate and format the output.

**Section 2: Excluding Columns**

When using jq to output JSON data, it is possible to exclude certain fields or columns from the output. This can be done by using the “-c” flag, which will cause jq to exclude the specified fields from the output.

**Section 3: Syntax**

The syntax for excluding columns from jq json output is as follows:

```
jq -c 'select(.field1 != null) | .field2, .field3'
```

In this example, the fields `field1` and `field4` are excluded from the output.

**Section 4: Examples**

Here is an example of how to exclude columns from jq json output:

```
jq -c 'select(.name != null) | .age, .city'
```

This will output the `age` and `city` fields, while excluding the `name` field.
