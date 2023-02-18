---
title: Decoding JSON with swift 4 using decodable where the keys are not known until the decoding process begins
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-18 00:00:00
updated_at: 2023-02-18 00:00:00
tldr: It is possible to decode JSON with unknown keys at decoding time using the CodingKey protocol and the keyDecodingStrategy of the JSONDecoder.
---

**Contents**

[TOC]

1. Introduction
Swift 4 Decodable is a powerful tool for decoding JSON data into Swift objects. It allows us to quickly and easily decode JSON data into Swift types with minimal code. One of the most powerful features of Decodable is that it allows us to decode JSON data even when the keys are not known until decoding time. This can be useful when dealing with dynamic JSON data or when dealing with APIs that have complex data structures.

2. Understanding the Problem
The problem with decoding JSON data when the keys are not known until decoding time is that the Decodable protocol requires us to specify the keys that we are expecting to decode. This means that if the keys are not known until decoding time, we must use a different approach to decode the data.

3. Solutions
There are several solutions to this problem. One approach is to use the `JSONDecoder` class. This class provides a `decode(_:from:)` method which allows us to decode JSON data without having to specify the expected keys. Another approach is to use the `JSONSerialization` class to parse the JSON data into a dictionary and then use the dictionary to create a Swift object. Finally, we can use a third-party library such as SwiftJSON to decode the JSON data into a Swift object without having to specify the expected keys.

4. Conclusion
Decoding JSON data when the keys are not known until decoding time can be a challenging task. However, with the help of the Decodable protocol, the JSONDecoder class, the JSONSerialization class, and third-party libraries such as SwiftJSON, it is possible to decode the data without having to specify the expected keys.
