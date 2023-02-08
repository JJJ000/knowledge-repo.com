---
title: Serializing a decimal object into JSON format using python
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: A Decimal object can be serialized in JSON using the json.dumps() method with the cls parameter set to the Decimal class.
---

**Contents**

[TOC]

# Serialization
The Decimal object can be serialized to JSON using the json.dumps() method. This method accepts an optional parameter called default which can be used to specify a custom serializer for complex objects. In this case, a custom serializer can be used to serialize the Decimal object to JSON.

# Custom Serializer
The custom serializer should accept an instance of the Decimal object and return a JSON-compatible representation of the object. The JSON-compatible representation can be a string or a dictionary. In this case, a string representation is used.

# Implementation
The following code shows the implementation of a custom serializer for Decimal objects:

```
import json
from decimal import Decimal

def decimal_serializer(obj):
    if isinstance(obj, Decimal):
        return str(obj)
    return obj

data = {
    'price': Decimal('10.99')
}

json_data = json.dumps(data, default=decimal_serializer)
```

# Output
The output of the above code is a JSON-encoded string with the Decimal object serialized as a string:

```
{"price": "10.99"}
```
