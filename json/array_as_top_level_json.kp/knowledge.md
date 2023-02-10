---
title: Is an array allowed as a top-level element in a JSON document?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Yes, an array can be top-level JSON-text in JSON.
---

**Contents**

[TOC]

##Yes

An array can be top-level JSON-text in JSON. A top-level array is a valid JSON document and can be used to represent a sequence of values, such as a list of numbers or strings. For example, the following JSON document is a valid top-level array:

```json
[1, 2, 3]
```

##No

An array cannot be top-level JSON-text in JSON if it contains objects. A top-level array must only contain values, such as numbers or strings, and not objects. For example, the following JSON document is not a valid top-level array:

```json
[{"name":"John"}, {"name":"Jane"}]
```

##Conclusion

In conclusion, an array can be top-level JSON-text in JSON as long as it only contains values, such as numbers or strings, and not objects.
