---
title: Using json.dumps to save utf-8 texts as utf-8 instead of as a \u escape sequence
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: Use the ensure\_ascii=False parameter when calling json.dumps to save UTF-8 texts in their raw form.
---

**Contents**

[TOC]

### Saving UTF-8 Texts

Saving UTF-8 texts with json.dumps can be done by setting the `ensure_ascii` parameter to `False` when calling the `dumps` method. This will ensure that the output is encoded as UTF-8 and not as a \u escape sequence. 

### Example

The following example shows how to use the `ensure_ascii` parameter to save UTF-8 texts.

```python
import json

data = {'name': 'John', 'age': 30, 'city': 'Berlin'}

# Saving UTF-8 texts
json_data = json.dumps(data, ensure_ascii=False)
```

### Output

The output of the above code will be a JSON string encoded as UTF-8 and not as a \u escape sequence.

```json
{
    "name": "John",
    "age": 30,
    "city": "Berlin"
}
```

### Conclusion

Saving UTF-8 texts with json.dumps in Python can be done by setting the `ensure_ascii` parameter to `False` when calling the `dumps` method. This will ensure that the output is encoded as UTF-8 and not as a \u escape sequence.
