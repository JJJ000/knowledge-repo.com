---
title: The object of django cannot be serialized as json
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: This error occurs when trying to serialize a Django model object directly to JSON.
---

**Contents**

[TOC]

Section 1: Introduction

Python is a widely used programming language that provides various libraries and modules to manipulate data. One of the most popular libraries for web development in Python is Django. While working with Django, developers often come across the error message "<Django object> is not JSON serializable". This error occurs when developers try to serialize an object in Django but that object cannot be converted to JSON data format.

In this article, we will explore the reasons behind this error and how to fix it.

Section 2: Reasons for the error message

The "not JSON serializable" error message is triggered when the object we are trying to serialize contains data that cannot be converted to a JSON object. This can happen for a few reasons:

1. Non-serializable types: Certain Python types cannot be converted to JSON format directly. For example, datetime objects, Decimal objects, and UUID objects are not serializable by default.

2. Nested Objects: If the object we are trying to serialize contains nested objects, which themselves contain non-serializable types, the serialization will fail.

3. Undefined or Circular References: If the object we are trying to serialize contains undefined reference or circular references, this error might occur.

Section 3: Solutions to the error message

Here are some solutions to fix the 'not JSON serializable' error:

1. Convert non-serializable types to serializable types: We can solve the serialization error by converting non-serializable types into a serializable format. For example, we can convert a datetime object into a string format, or use float instead of Decimal objects.

2. Use Django's built-in serialization tools: Django provides built-in serialization tools that can handle certain non-serializable types, such as datetime objects. We can use these tools to serialize objects in Django.

3. Exclude non-serializable data: If we are unable to convert non-serializable data to serializable data, we can exclude the problematic data from serialization. We can do this by using Django's serializer's exclude and only arguments.

4. Use third-party libraries: There are many third-party libraries available in Python that can help to serialize non-serializable objects. For example, the Django REST framework has a built-in serializer, which converts Django objects into JSON format.

Section 4: Conclusion

In conclusion, the "not JSON serializable" error message in Django occurs when an object contains non-serializable data. We can fix this error by converting non-serializable data into serializable data, using Django's built-in serialization tools, excluding non-serializable data, or using third-party libraries. By understanding the reasons behind this error and applying the solutions mentioned above, we can easily fix the "not JSON serializable" error message in Django.
