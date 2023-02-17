---
title: What is the process for decoding JSON in flutter?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: Use the built-in jsonDecode() method from dartconvert to decode JSON in Flutter.
---

**Contents**

[TOC]

1. **Import Packages:**

In order to decode JSON in Flutter, you must first import the `dart:convert` package.

```dart
import 'dart:convert';
```

2. **Decode JSON:**

Once the package is imported, you can use the `jsonDecode()` method to decode the JSON string.

```dart
String jsonString = '{"name": "John", "age": 20}';
Map<String, dynamic> userData = jsonDecode(jsonString);
```

3. **Accessing Data:**

Once the JSON is decoded, you can access the data using the `[]` operator.

```dart
String name = userData['name'];
int age = userData['age'];
```

4. **Handling Errors:**

It is important to handle any errors that may occur when decoding the JSON. You can do this by wrapping the `jsonDecode()` method in a `try-catch` block.

```dart
try {
  Map<String, dynamic> userData = jsonDecode(jsonString);
  String name = userData['name'];
  int age = userData['age'];
} catch(e) {
  print(e);
}
```
