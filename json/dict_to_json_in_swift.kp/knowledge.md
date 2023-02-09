---
title: Transform a dictionary into JSON format in swift
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: It is possible to convert a Dictionary to JSON in Swift using the JSONSerialization class.
---

**Contents**

[TOC]

## Section 1: Convert Dictionary to JSON

Swift provides a built-in method to convert a Dictionary to JSON. To convert a Dictionary to JSON, use `JSONSerialization.data(withJSONObject:options:)` with `.prettyPrinted` as the options parameter.

The following example shows how to convert a Dictionary to JSON in Swift:

```swift
let dict: [String: Any] = ["name": "John", "age": 25]

if let jsonData = try? JSONSerialization.data(withJSONObject: dict, options: .prettyPrinted) {
    let jsonString = String(data: jsonData, encoding: .utf8)
    print(jsonString!)
}
```

The above example will print the following JSON string:

```json
{
  "name" : "John",
  "age" : 25
}
```

## Section 2: Convert JSON to Dictionary

Swift provides a built-in method to convert a JSON string to a Dictionary. To convert a JSON string to a Dictionary, use `JSONSerialization.jsonObject(with:options:)` with `.mutableContainers` as the options parameter.

The following example shows how to convert a JSON string to a Dictionary in Swift:

```swift
let jsonString = "{\"name\":\"John\",\"age\":25}"

if let jsonData = jsonString.data(using: .utf8) {
    if let dict = try? JSONSerialization.jsonObject(with: jsonData, options: .mutableContainers) as? [String: Any] {
        print(dict)
    }
}
```

The above example will print the following Dictionary:

```
["name": "John", "age": 25]
```

## Section 3: Handling Errors

When converting a Dictionary to JSON or a JSON string to a Dictionary, it is important to handle any errors that may occur.

When converting a Dictionary to JSON, use `try?` to handle any errors that may occur.

When converting a JSON string to a Dictionary, use `try?` to handle any errors that may occur.

## Section 4: Conclusion

In summary, Swift provides built-in methods to convert a Dictionary to JSON or a JSON string to a Dictionary. When using these methods, it is important to handle any errors that may occur.
