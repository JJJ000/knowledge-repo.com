---
title: Converting JSON into an abstract class
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: It is not possible to deserialize JSON to an abstract class.
---

**Contents**

[TOC]

#### Section 1: Abstract Classes
An abstract class is a class that cannot be instantiated and is used as a base class for other classes. Abstract classes are used to define the interface and the structure of a class hierarchy.

#### Section 2: Deserializing JSON
Deserializing JSON is the process of converting JSON data into a native object. This process is done by using a library such as Jackson or Gson to parse the JSON data and create the corresponding object.

#### Section 3: Deserializing JSON to Abstract Classes
Deserializing JSON to an abstract class is possible, but it requires a bit more work than deserializing to a concrete class. This is because the abstract class does not have any implementation details and the library needs to be able to determine which concrete class to instantiate.

#### Section 4: Implementing Deserialization
In order to deserialize JSON to an abstract class, you need to provide the library with a custom deserializer. The deserializer should be able to determine which concrete class to instantiate based on the data in the JSON. The deserializer should also be able to create an instance of the concrete class and populate it with the data from the JSON.
