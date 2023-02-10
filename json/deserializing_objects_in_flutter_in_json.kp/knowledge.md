---
title: What is the process of converting a list of objects from JSON to a usable format in flutter?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use the jsonDecode() method from the dartconvert library to deserialize a list of objects from JSON in Flutter.
---

**Contents**

[TOC]

### Section 1: Create the Model

The first step in deserializing a list of objects from JSON in flutter is to create a model class for the objects. This model class should contain all the properties of the objects that you are trying to deserialize. For example, if you are deserializing a list of books, the model class should contain properties such as title, author, and ISBN.

### Section 2: Create the Deserializer

The next step is to create a deserializer class. This class should have a static method that takes a JSON string as an argument and returns a list of model objects. The deserializer should use the built-in jsonDecode() method to parse the JSON string and then use the model class to create a list of objects.

### Section 3: Call the Deserializer

Once the model and deserializer classes have been created, the next step is to call the deserializer. This can be done by passing the JSON string to the deserializer method and then storing the result in a variable.

### Section 4: Use the Deserialized List

Finally, the deserialized list can be used in your application. This can be done by accessing the list variable and then looping through it to access the individual objects. The individual objects can then be used in whatever way you need.
