---
title: What is the process of converting a sqlalchemy result to json?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Use the json.dumps() function to serialize SqlAlchemy result to JSON.
---

**Contents**

[TOC]

# Section 1: Import Libraries

```python
import json
from sqlalchemy.ext.declarative import DeclarativeMeta
```

# Section 2: Define Serializer

```python
class AlchemyEncoder(json.JSONEncoder):

    def default(self, obj):
        if isinstance(obj.__class__, DeclarativeMeta):
            # an SQLAlchemy class
            fields = {}
            for field in [x for x in dir(obj) if not x.startswith('_') and x != 'metadata']:
                data = obj.__getattribute__(field)
                try:
                    json.dumps(data) # this will fail on non-encodable values, like other classes
                    fields[field] = data
                except TypeError:
                    fields[field] = None
            # a json-encodable dict
            return fields

        return json.JSONEncoder.default(self, obj)
```

# Section 3: Serialize Result

```python
result = session.query(MyModel).all()
json.dumps(result, cls=AlchemyEncoder)
```

# Section 4: Output

This will return a JSON string of the serialized SQLAlchemy result.
