---
title: Using django-rest-framework 3.0, create or update data within a nested serializer
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: The create or update operation can be done using the `partial=True` argument when instantiating a serializer.
---

**Contents**

[TOC]

1. **Creating a Nested Serializer**
   To create a nested serializer, you need to create a serializer class that will contain the nested serializer as a field. For example, if you have a model with a foreign key to another model, you can create a nested serializer to represent the relationship:

```python
class ParentSerializer(serializers.ModelSerializer):
    child = ChildSerializer()
    class Meta:
        model = Parent
        fields = ('id', 'name', 'child')
```

2. **Updating a Nested Serializer**
   To update a nested serializer, you need to use the `update()` method of the serializer. The `update()` method takes a dictionary of data as its argument, and it will update the serializer's fields with the data provided. The nested serializer can be updated by passing the data for the nested serializer as a dictionary within the data dictionary. For example:

```python
data = {
    'name': 'Parent Name',
    'child': {
        'name': 'Child Name',
        'age': 5
    }
}

serializer = ParentSerializer()
serializer.update(data)
```

3. **Handling Nested Serializer Validation**
   When updating a nested serializer, it is important to ensure that the data is valid. To do this, the `validate()` method of the serializer can be used. The `validate()` method takes a dictionary of data as its argument, and it will validate the data against the serializer's fields. If the data is invalid, it will raise a `ValidationError` exception. For example:

```python
data = {
    'name': 'Parent Name',
    'child': {
        'name': 'Child Name',
        'age': 'invalid age'
    }
}

serializer = ParentSerializer()
try:
    serializer.validate(data)
except ValidationError as e:
    print(e)
```

4. **Handling Nested Serializer Errors**
   If the `validate()` method of the serializer raises a `ValidationError` exception, it will contain a list of errors for each field that was invalid. To handle the errors, the `errors` attribute of the serializer can be used. The `errors` attribute contains a dictionary of errors for each field, and can be used to display the errors to the user. For example:

```python
data = {
    'name': 'Parent Name',
    'child': {
        'name': 'Child Name',
        'age': 'invalid age'
    }
}

serializer = ParentSerializer()
try:
    serializer.validate(data)
except ValidationError as e:
    print(serializer.errors)
```
