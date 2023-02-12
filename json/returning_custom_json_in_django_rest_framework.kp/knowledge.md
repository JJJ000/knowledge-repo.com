---
title: What is the best way to output custom JSON using django rest framework?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: You can return custom JSON in Django REST Framework by overriding the default serializer`s `to\_representation` method.
---

**Contents**

[TOC]

1. Create a Serializer 

In order to return custom JSON in Django REST Framework, you must create a Serializer. A Serializer is a class that takes a Model or QuerySet instance and turns it into JSON, XML or other content types. It is used to convert the model data into a format that can be easily rendered into a view.

2. Create a View 

Once you have created a Serializer, you must create a View to use it. The View is responsible for taking the data from the Serializer and rendering it in the desired format. You can use the Django REST Framework's generic views to make this process easier.

3. Use the Serializer 

Once you have created a View, you can use the Serializer to render the data into the desired format. The Serializer will take the data from the Model or QuerySet instance and convert it into JSON, XML or other content types.

4. Return the Data 

Finally, you can return the data from the Serializer in the desired format. You can return the data as a Response object or as a JSON string.
