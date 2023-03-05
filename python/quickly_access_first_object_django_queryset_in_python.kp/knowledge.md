---
title: What is the quickest method to obtain the initial object from a queryset in django?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Use the .first() method on the queryset to get the first object.
---

**Contents**

[TOC]

## Using the `first()` method

One of the easiest and fastest ways to get the first object from a queryset in Django is to use the `first()` method. This method returns the first object in the queryset if it exists, or `None` if the queryset is empty. Here's an example of using the `first()` method:

```
first_object = MyModel.objects.first()
```

In the example above, we're fetching the first object from the `MyModel` queryset and assigning it to the `first_object` variable. If the queryset is empty, `first_object` will be set to `None`.

## Using indexing

Another way to get the first object from a queryset in Django is to use indexing. You can treat the queryset as a list-like object and use the `[0]` index to get the first object. Here's an example:

```
result_set = MyModel.objects.filter(some_field=some_value)
if result_set:
    first_object = result_set[0]
else:
    first_object = None
```

In the example above, we're filtering the `MyModel` queryset based on some criteria, then checking if the resulting queryset is not empty (i.e. it contains at least one object). If it's not empty, we're assigning the first object to the `first_object` variable using the `[0]` index. If the queryset is empty, `first_object` will be set to `None`.

## Using the `get()` method

If you know that your queryset can only contain one object (i.e. you're filtering by a unique field), you can use the `get()` method to retrieve the object. This method raises a `DoesNotExist` exception if the queryset is empty, or a `MultipleObjectsReturned` exception if the queryset contains more than one object. Here's an example:

```
try:
    first_object = MyModel.objects.get(unique_field=unique_value)
except MyModel.DoesNotExist:
    first_object = None
```

In the example above, we're using the `get()` method to retrieve the object that matches the `unique_field` value. If the queryset is empty, the `DoesNotExist` exception will be raised and we'll assign `None` to the `first_object` variable. If the queryset contains more than one object, the `MultipleObjectsReturned` exception will be raised.

## Conclusion

There are several ways to get the first object from a queryset in Django. The best approach depends on your specific use case and the queryset that you're working with. For most cases, using the `first()` method is the easiest and fastest way to get the first object. If you need more control or flexibility, you can use indexing or the `get()` method.
