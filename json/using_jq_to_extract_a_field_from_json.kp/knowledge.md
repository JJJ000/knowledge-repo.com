---
title: Retrieve a particular element from JSON output using jq
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: jq can be used to extract a specific field from a JSON output by using a selector expression.
---

**Contents**

[TOC]

### Section 1 - Installing jq

In order to use jq to extract a field from JSON output, you must first install jq on your system. jq is available for download from the official [jq website](https://stedolan.github.io/jq/). Once you have downloaded and installed jq, you can begin using it to extract fields from JSON output.

### Section 2 - Understanding JSON

Before you can use jq to extract a field from JSON output, it is important to understand the structure of JSON. JSON is a data format that is commonly used to exchange information between different systems. It consists of key-value pairs that are organized into a hierarchical structure. This hierarchical structure allows you to easily access specific fields from the data.

### Section 3 - Using jq

Once you have installed jq and understand the structure of JSON, you can use jq to extract a specific field from JSON output. To do this, you will need to provide jq with a query that specifies the path to the field you want to extract. For example, if you wanted to extract the "name" field from the following JSON output:

```json
{
  "person": {
    "name": "John Doe",
    "age": 34
  }
}
```

You could use the following jq query:

```
jq '.person.name'
```

This query will return the value of the "name" field, which is "John Doe".

### Section 4 - Outputting the Result

Once you have used jq to extract the field you want, you can output the result in a variety of formats. By default, jq will output the result as a JSON string. However, you can also output the result as a plain-text string, or as a list or array. To output the result in a different format, you can use the -r or --raw-output option. For example, to output the result as a plain-text string, you could use the following command:

```
jq -r '.person.name'
```

This command will output the value of the "name" field as a plain-text string: "John Doe".
