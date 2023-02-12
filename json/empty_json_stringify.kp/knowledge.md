---
title: Json.stringify returning an empty array
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: JSON.stringify returns an empty array as an empty string.
---

**Contents**

[TOC]

### Empty Array

JSON.stringify will return an empty array `[]` when the array is empty, meaning it contains no elements.

### Example

For example, if we have an empty array:

```
let array = [];
```

We can use JSON.stringify to convert it to a JSON string:

```
JSON.stringify(array); // returns "[]"
```

### Usage

This can be useful when sending an empty array to an API endpoint, as the API may require an array to be present even if it is empty.

### Alternatives

If you need to send an empty array, but don't want to use JSON.stringify, you can also send an empty string `""` or `null`.
