---
title: What is the best way to omit properties when using swift codable?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use the CodingKeys enum to specify which properties should be excluded from Codable.
---

**Contents**

[TOC]

#### Section 1: Excluding Properties from Encoding

When encoding an object to JSON using Swift's Codable protocol, you can exclude certain properties from being encoded by adding the `CodingKeys` enum and overriding the `encode(_:forKey:)` method.

#### Section 2: Adding the CodingKeys Enum

To exclude a property from encoding, add an enum called `CodingKeys` to your class. This enum should conform to the `CodingKey` protocol and should list all of the properties in your class. Any properties you want to exclude from encoding should be marked with the `.ignore` case.

For example, if you wanted to exclude the `name` property from encoding, your `CodingKeys` enum would look like this:

```
enum CodingKeys: CodingKey {
    case id
    case age
    case name // excluded from encoding
}
```

#### Section 3: Overriding encode(_:forKey:)

Next, you need to override the `encode(_:forKey:)` method in your class. This method should check the `CodingKeys` enum to see if the property should be encoded. If the property should be excluded, the method should return without encoding the property.

For example, if you wanted to exclude the `name` property, your `encode(_:forKey:)` method would look like this:

```
override func encode(to encoder: Encoder) throws {
    var container = encoder.container(keyedBy: CodingKeys.self)
    try container.encode(id, forKey: .id)
    try container.encode(age, forKey: .age)
    if CodingKeys(stringValue: key.stringValue) != .name { // exclude name
        try container.encode(name, forKey: .name)
    }
}
```

#### Section 4: Decoding Excluded Properties

When decoding an object from JSON using Swift's Codable protocol, the excluded properties will still be decoded. If you want to exclude them from decoding, you can do so by overriding the `init(from:)` method and checking the `CodingKeys` enum to see if the property should be decoded. If the property should be excluded, you can skip it.
