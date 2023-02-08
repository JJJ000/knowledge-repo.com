---
title: Does the order of elements in a JSON list stay the same?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Yes, the order of elements in a JSON list is preserved in Javascript.
---

**Contents**

[TOC]

### Yes

The order of elements in a JSON list is preserved in Javascript. This means that when a JSON list is converted into a Javascript array, the elements will appear in the same order as they were in the original JSON list.

### How

When a JSON list is converted into a Javascript array, the elements are stored in the same order as they were in the original JSON list. This is because the Javascript interpreter will iterate through the elements in the same order as they were presented in the JSON list.

### Example

For example, if the following JSON list is converted into a Javascript array:

```
[1, 2, 3, 4, 5]
```

The resulting Javascript array will contain the elements in the same order as they were in the JSON list:

```
[1, 2, 3, 4, 5]
```
