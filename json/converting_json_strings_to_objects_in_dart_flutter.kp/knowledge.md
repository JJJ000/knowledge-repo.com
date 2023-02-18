---
title: What is the best way to turn a JSON string into a JSON object in dart flutter?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-18 00:00:00
updated_at: 2023-02-18 00:00:00
tldr: Use the `jsonDecode()` method to convert a JSON string to a JSON object in Dart/Flutter.
---

**Contents**

[TOC]

# Section 1: Importing the 'json' Package
In order to convert a JSON string to a JSON object in Dart/Flutter, the first step is to import the `json` package. This can be done by adding the following code to the top of your file:

```dart
import 'dart:convert';
```

# Section 2: Decoding the JSON String
Once the `json` package has been imported, the next step is to decode the JSON string. This can be done using the `jsonDecode()` method, which takes a JSON string as an argument and returns a `Map<String, dynamic>` object.

For example:

```dart
String jsonString = '{"name":"John","age":30}';
Map<String, dynamic> jsonObject = jsonDecode(jsonString);
```

# Section 3: Accessing the JSON Object
Once the JSON string has been decoded, it can be accessed like any other `Map<String, dynamic>` object.

For example:

```dart
String name = jsonObject["name"];
int age = jsonObject["age"];
```

# Section 4: Outputting the JSON Object
Finally, the JSON object can be outputted as a string using the `jsonEncode()` method. This method takes a `Map<String, dynamic>` object as an argument and returns a JSON string.

For example:

```dart
String jsonString = jsonEncode(jsonObject);
```
