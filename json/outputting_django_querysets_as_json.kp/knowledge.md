---
title: What is the best way to display a django queryset as json?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use the `.values()` method to output a Django queryset as JSON.
---

**Contents**

[TOC]

## Section 1: Import the Necessary Libraries

In order to output a Django queryset as JSON, you will need to import the necessary libraries. This includes the `json` library from Python and the `serializers` library from Django:

```python
import json
from django.core import serializers
```

## Section 2: Create the QuerySet

Next, you will need to create the QuerySet that you want to output as JSON. This can be done using the `.filter()` method of the Django ORM:

```python
queryset = MyModel.objects.filter(field1=value1, field2=value2)
```

## Section 3: Serialize the QuerySet

Once the QuerySet has been created, you can serialize it using the `serializers.serialize()` method:

```python
data = serializers.serialize('json', queryset)
```

## Section 4: Output the JSON

Finally, you can output the serialized data as JSON using the `json.dumps()` method:

```python
json_data = json.dumps(data)
print(json_data)
```
