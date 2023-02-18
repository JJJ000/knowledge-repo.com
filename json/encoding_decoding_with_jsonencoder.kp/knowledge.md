---
title: Convert an array of objects that follow a certain protocol into a JSON format and back using jsonencoder
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-18 00:00:00
updated_at: 2023-02-18 00:00:00
tldr: Yes, it is possible to encode/decode an array of types conforming to a protocol with JSONEncoder in JSON.
---

**Contents**

[TOC]

# Section 1: Encoding

JSONEncoder can be used to encode an array of types conforming to a protocol. To do this, the array must be cast to an array of `Encodable` objects. This can be done using the `map` function.

```swift
let array: [MyProtocol] = [MyObject1(), MyObject2()]
let encodableArray = array.map { $0 as Encodable }
let encoder = JSONEncoder()
let data = try encoder.encode(encodableArray)
```

# Section 2: Decoding

JSONDecoder can be used to decode an array of types conforming to a protocol. To do this, the array must be cast to an array of `Decodable` objects. This can be done using the `map` function.

```swift
let decoder = JSONDecoder()
let decodableArray = try decoder.decode([MyProtocol].self, from: data)
let array = decodableArray.map { $0 as MyProtocol }
```

# Section 3: Customizing Encoding

If you need to customize the encoding process, you can create a custom `JSONEncoder` subclass and override the `encode` method. This method takes an array of `Encodable` objects and returns a `Data` object.

```swift
class MyEncoder: JSONEncoder {
    override func encode<T>(_ value: T) throws -> Data where T : Encodable {
        // Customize encoding here
    }
}
```

# Section 4: Customizing Decoding

If you need to customize the decoding process, you can create a custom `JSONDecoder` subclass and override the `decode` method. This method takes a `Data` object and returns an array of `Decodable` objects.

```swift
class MyDecoder: JSONDecoder {
    override func decode<T>(_ type: T.Type, from data: Data) throws -> T where T : Decodable {
        // Customize decoding here
    }
}
```
