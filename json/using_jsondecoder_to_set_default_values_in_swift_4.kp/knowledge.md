---
title: Can jsondecoder in swift 4 use a default value for missing keys instead of making them optional properties?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: No, missing keys cannot use a default value instead of being optional properties in JSON when using JSONDecoder in Swift 4.
---

**Contents**

[TOC]

## Option 1: Use Swift's Optional Chaining

Swift's optional chaining can be used to provide a default value when the key is missing from the JSON data. This involves using the `??` operator to provide a default value for the optional property. For example:

```swift
let jsonData = // JSON data from server
let decoder = JSONDecoder()

do {
    let model = try decoder.decode(MyModel.self, from: jsonData)
    let value = model.optionalProperty ?? "defaultValue"
} catch {
    // handle errors
}
```

## Option 2: Create a Custom Decoder

A custom decoder can be used to provide a default value when the key is missing from the JSON data. This involves creating a custom decoder that implements the `Decoder` protocol and overriding the `decode` method. For example:

```swift
struct MyDecoder: Decoder {
    func decode<T>(_ type: T.Type, from data: Data) throws -> T where T : Decodable {
        let decoder = JSONDecoder()
        let model = try decoder.decode(MyModel.self, from: data)
        let value = model.optionalProperty ?? "defaultValue"
        return value as! T
    }
}
```

## Option 3: Create a Custom Coding Key

A custom coding key can be used to provide a default value when the key is missing from the JSON data. This involves creating a custom coding key that implements the `CodingKey` protocol and overriding the `decode` method. For example:

```swift
struct MyCodingKey: CodingKey {
    func decode<T>(_ type: T.Type, from data: Data) throws -> T where T : Decodable {
        let decoder = JSONDecoder()
        let model = try decoder.decode(MyModel.self, from: data)
        let value = model.optionalProperty ?? "defaultValue"
        return value as! T
    }
}
```

## Option 4: Use a Third-Party Library

Third-party libraries such as [SwiftyJSON](https://github.com/SwiftyJSON/SwiftyJSON) can be used to provide a default value when the key is missing from the JSON data. For example:

```swift
let json = // JSON data from server
let jsonObject = JSON(data: json)
let value = jsonObject["optionalProperty"].stringValue ?? "defaultValue"
```
