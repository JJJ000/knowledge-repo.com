---
title: Convert JSON / nsdictionary data into swift objects
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-18 00:00:00
updated_at: 2023-02-18 00:00:00
tldr: JSON can be deserialized into Swift objects by using the JSONDecoder class.
---

**Contents**

[TOC]

**Section 1: Deserialize JSON to Swift Objects**

The most common way to deserialize JSON to Swift objects is to use the Codable protocol. The Codable protocol is a combination of the Encodable and Decodable protocols. It allows us to convert JSON data into Swift objects and vice versa. To use the Codable protocol, we must define a struct or class with all the properties that we want to map from the JSON, and then use the JSONDecoder class to decode the JSON data into an instance of our struct or class.

**Section 2: Deserialize NSDictionary to Swift Objects**

NSDictionary can also be deserialized to Swift objects. To do this, we can use the DictionaryDecoder class. This class is part of the Swift Core Libraries and it allows us to convert NSDictionary objects into Swift objects. To use the DictionaryDecoder class, we must define a struct or class with all the properties that we want to map from the NSDictionary, and then use the DictionaryDecoder class to decode the NSDictionary into an instance of our struct or class.

**Section 3: Benefits of Deserializing JSON and NSDictionary to Swift Objects**

Deserializing JSON and NSDictionary to Swift objects has many benefits. It allows us to take complex data structures and easily convert them into Swift objects. This makes it easier to work with the data in our applications. It also allows us to easily serialize the data back to a JSON or NSDictionary format when needed.

**Section 4: Limitations of Deserializing JSON and NSDictionary to Swift Objects**

Although deserializing JSON and NSDictionary to Swift objects has many benefits, there are also some limitations. For example, the Codable protocol does not allow for custom mapping of data, so the data must be mapped exactly as it is in the JSON or NSDictionary. Additionally, the DictionaryDecoder class does not support nested objects, so if the data is nested it must be flattened before it can be deserialized.
