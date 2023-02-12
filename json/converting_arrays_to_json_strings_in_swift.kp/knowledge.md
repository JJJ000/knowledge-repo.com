---
title: Create a JSON string from an array in swift
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: You can convert an array to a JSON string in Swift by using the JSONSerialization class.
---

**Contents**

[TOC]

# Section 1: Overview

JSON (JavaScript Object Notation) is a lightweight data-interchange format used for exchanging data between a server and a client. It is a text-based, human-readable format that is used to represent structured data. In Swift, the Foundation framework provides the necessary methods for converting a JSON string into an array.

# Section 2: Convert JSON String to Array

The Foundation framework provides the `JSONSerialization` class, which contains the `jsonObject(with:options:)` method. This method takes a JSON string and an `JSONSerialization.ReadingOptions` option as parameters and returns an array or dictionary. To convert the JSON string to an array, pass in the `JSONSerialization.ReadingOptions.mutableContainers` option.

# Section 3: Example

The following example shows how to convert a JSON string to an array in Swift:

```swift
let jsonString = "{\"name\":\"John\",\"age\":30,\"city\":\"New York\"}"

if let data = jsonString.data(using: .utf8) {
    do {
        if let jsonArray = try JSONSerialization.jsonObject(with: data, options: .mutableContainers) as? [String: Any] {
            // jsonArray is an array of [String: Any]
        }
    } catch {
        print(error.localizedDescription)
    }
}
```

# Section 4: Conclusion

Converting a JSON string to an array in Swift is a straightforward process. The `JSONSerialization` class provides the necessary methods to parse the JSON string into an array. Once the JSON string is parsed, it can be used to access the data contained within the array.
