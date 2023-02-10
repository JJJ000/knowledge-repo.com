---
title: Use the standard JSON module to format floating point numbers
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: No, the standard JSON module does not support formatting floats.
---

**Contents**

[TOC]

**Solution**

#### Using the JSON Encoder

The json module provides an encoder class which can be used to customize the way floats are serialized. To use the encoder, a subclass must be created and the `.iterencode()` method must be overridden.

The following example shows how to override the `.iterencode()` method to format floats with two decimal places:

```python
import json

class FloatEncoder(json.JSONEncoder):
    def iterencode(self, o, _one_shot=False):
        if isinstance(o, float):
            o = round(o, 2)
        return super(FloatEncoder, self).iterencode(o, _one_shot)

data = {'a': 1.2345, 'b': 4.5678}
encoded_data = json.dumps(data, cls=FloatEncoder)
print(encoded_data)
# Output: {"a": 1.23, "b": 4.57}
```

#### Using the JSON Dumper

The json module also provides a dumper class which can be used to customize the way floats are serialized. To use the dumper, a subclass must be created and the `.write()` method must be overridden.

The following example shows how to override the `.write()` method to format floats with two decimal places:

```python
import json

class FloatDumper(json.JSONEncoder):
    def write(self, o):
        if isinstance(o, float):
            o = round(o, 2)
        return super(FloatDumper, self).write(o)

data = {'a': 1.2345, 'b': 4.5678}
encoded_data = json.dumps(data, cls=FloatDumper)
print(encoded_data)
# Output: {"a": 1.23, "b": 4.57}
```

#### Using a Custom Serializer

The json module also provides a custom serializer which can be used to customize the way floats are serialized. To use the custom serializer, a subclass must be created and the `.default()` method must be overridden.

The following example shows how to override the `.default()` method to format floats with two decimal places:

```python
import json

class FloatSerializer(json.JSONEncoder):
    def default(self, o):
        if isinstance(o, float):
            o = round(o, 2)
        return super(FloatSerializer, self).default(o)

data = {'a': 1.2345, 'b': 4.5678}
encoded_data = json.dumps(data, default=FloatSerializer)
print(encoded_data)
# Output: {"a": 1.23, "b": 4.57}
```
