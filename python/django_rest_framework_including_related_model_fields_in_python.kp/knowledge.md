---
title: What is the process for incorporating related model fields with django rest framework?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Use nested serializers to include related model fields in Django Rest Framework.
---

**Contents**

[TOC]

## Importing Dependencies

To begin, we need to import the necessary dependencies such as serializer and view classes from Django Rest Framework. For example:

```python
from rest_framework import serializers, viewsets
```

## Serializers

Next, we need to define serializers to return related models. To include related model fields in Django Rest Framework, we can use nested serializers or the `depth` meta option. Here is an example using nested serializers:

```python
class AuthorSerializer(serializers.ModelSerializer):
    class Meta:
        model = Author
        fields = ('id', 'name', 'books')
    
class BookSerializer(serializers.ModelSerializer):
    author = AuthorSerializer()
    
    class Meta:
        model = Book
        fields = ('id', 'title', 'author')
```

In this example, `BookSerializer` includes the `author` field which is serialized using the `AuthorSerializer`. This will return the author's `id`, `name`, and all of their `books`.

Alternatively, we can use the `depth` meta option to include all related model fields up to a certain level. Here is an example:

```python
class BookSerializer(serializers.ModelSerializer):
    class Meta:
        model = Book
        fields = ('id', 'title', 'author')
        depth = 1
```

In this example, `depth=1` includes the author's `id`, `name`, and all of their `books`.

## ViewSets

Finally, we need a viewset to handle the request and return the serialized data. Here is an example:

```python
class BookViewSet(viewsets.ModelViewSet):
    queryset = Book.objects.all()
    serializer_class = BookSerializer
```

This viewset simply declares the `BookSerializer` as the serializer class and the `queryset` as all `Book` objects. When a request is made to the viewset, the objects will be serialized and returned in the response.

## Conclusion

By using serializers to return related model fields and viewsets to handle requests, we can easily include related model data in responses using Django Rest Framework.
