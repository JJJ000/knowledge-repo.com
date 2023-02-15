---
title: Decoding values that can be either an int or a string using codable
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-15 00:00:00
updated_at: 2023-02-15 00:00:00
tldr: You can use a custom CodingKey enum that has both a String and an Int case to decode values that are sometimes an Int and other times a String in JSON.
---

**Contents**

[TOC]

##### Handling Int and String Values

If the value in the JSON can be either an Int or a String, the data type of the corresponding Swift property should be `Any`. This data type can represent any type of value, including Int and String.

##### Decoding the JSON

When decoding the JSON, the `JSONDecoder` will attempt to match the type of the property to the type of the value in the JSON. When the types don't match, the `JSONDecoder` will throw an error. To avoid this, we can use the `decodeIfPresent` method, which will return an optional value. If the type of the value in the JSON doesn't match the type of the property, the `decodeIfPresent` method will return `nil` instead of throwing an error.

##### Encoding the JSON

When encoding the JSON, the `JSONEncoder` will automatically convert the Swift property to the corresponding type in the JSON. If the property is of type `Any`, the `JSONEncoder` will automatically detect the type of the value and encode it as the corresponding type in the JSON.

##### Example

For example, given the following JSON:

```json
{
  "name": "John",
  "age": 30
}
```

We can define a `Person` struct like this:

```swift
struct Person: Codable {
  let name: String
  let age: Any
}
```

When decoding the JSON, the `JSONDecoder` will match the type of the `name` property (`String`) to the type of the `name` value in the JSON (`String`). The `JSONDecoder` will also match the type of the `age` property (`Any`) to the type of the `age` value in the JSON (`Int`).

When encoding the JSON, the `JSONEncoder` will automatically encode the `name` property as a `String` and the `age` property as an `Int`.
