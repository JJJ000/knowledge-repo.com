---
title: How can I decode a JSON dictionary property in swift using the decodable protocol?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Decode a JSON dictionary in Swift using the Decodable protocol by implementing the decode(from) method.
---

**Contents**

[TOC]

## Section 1: Implementing the Decodable Protocol

The `Decodable` protocol is used to decode a property with type of JSON dictionary in Swift. To implement the protocol, you need to create a struct or class that conforms to `Decodable`. The struct or class should have properties that match the keys of the JSON dictionary.

## Section 2: Decoding the JSON Dictionary

Once the struct or class is created, you can decode the JSON dictionary by using the `JSONDecoder` class. The `JSONDecoder` class has a `decode` method that takes two arguments: the type of the struct or class that conforms to `Decodable` and the JSON dictionary. The `decode` method will return an instance of the struct or class with the properties populated with the values from the JSON dictionary.

## Section 3: Handling Errors

When decoding the JSON dictionary, there may be errors. The `decode` method will throw an error if there is a problem decoding the JSON dictionary. To handle errors, you should use a `do`-`catch` statement. The `catch` statement should contain an `error` parameter that can be used to determine what type of error occurred and how to handle it.

## Section 4: Example

Here is an example of how to decode a JSON dictionary in Swift with the `Decodable` protocol:

```swift
struct Person: Decodable {
    let name: String
    let age: Int
}

let jsonDictionary: [String: Any] = ["name": "John", "age": 30]

do {
    let decoder = JSONDecoder()
    let person = try decoder.decode(Person.self, from: jsonDictionary)
    print(person.name) // Prints "John"
    print(person.age) // Prints "30"
} catch {
    print("Error decoding JSON dictionary: \(error)")
}
```
