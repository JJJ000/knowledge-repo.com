---
title: An easy and neat method for transforming a JSON string into an object in swift
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use the built-in JSONDecoder to convert a JSON string to an object.
---

**Contents**

[TOC]

### Step 1: Create Data from JSON String

In order to convert a JSON string to an object, we must first create a `Data` object from the JSON string. We can do this using the `data(using:)` initializer on `String`.

```swift
let jsonString = """
{
    "name": "John Doe",
    "age": 42
}
"""

let jsonData = jsonString.data(using: .utf8)
```

### Step 2: Decode JSON Data

Once we have a `Data` object from our JSON string, we can use the `JSONDecoder` to decode the data into an object. We can do this using the `decode(_:from:)` method on `JSONDecoder`.

```swift
struct Person: Codable {
    let name: String
    let age: Int
}

let decoder = JSONDecoder()
let person = try decoder.decode(Person.self, from: jsonData)
```

### Step 3: Access Properties

Once we have decoded the JSON data into an object, we can access the properties of that object.

```swift
print(person.name) // prints "John Doe"
print(person.age) // prints 42
```

### Step 4: Use Object

Finally, we can use the object as we would any other object in our program.

```swift
let greeting = "Hello, \(person.name)!"
print(greeting) // prints "Hello, John Doe!"
```
