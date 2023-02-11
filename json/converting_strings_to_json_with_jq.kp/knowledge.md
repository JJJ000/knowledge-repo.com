---
title: Transform a string into a JSON object using jq
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: Use the `fromjson` function to convert a string to JSON in jq.
---

**Contents**

[TOC]

### Section 1: Overview

jq is a lightweight, command-line JSON processor. It can be used to filter, parse, and transform JSON data. jq can also be used to convert a string to JSON.

### Section 2: Prerequisites

Before converting a string to JSON, the string must be valid JSON syntax. This means that the string must be in the correct format, with quotes around keys and values, and with commas separating key-value pairs.

### Section 3: Steps

1. Use jq's `fromjson` filter to convert the string to JSON.
2. Use jq's `tojson` filter to format the output as valid JSON.

### Section 4: Example

To convert a string to JSON using jq, the following command can be used:

```
$ echo '{"key1": "value1", "key2": "value2"}' | jq fromjson | jq tojson
```

The output of this command will be a valid JSON string:

```
{
  "key1": "value1",
  "key2": "value2"
}
```
