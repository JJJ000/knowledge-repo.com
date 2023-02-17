---
title: What is the process for transforming JSON serialized data into an nsdictionary?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: Use the NSJSONSerialization class to convert JSON serialized data to an NSDictionary.
---

**Contents**

[TOC]

# Section 1: Deserializing JSON

JSON (JavaScript Object Notation) is a lightweight data-interchange format. It is often used to exchange data between a server and web applications. To convert JSON serialized data to an NSDictionary (objective-C) or Dictionary (Swift), we need to deserialize the JSON data. 

# Section 2: Using JSONSerialization

In both Objective-C and Swift, the JSONSerialization class is used to convert JSON data into an NSDictionary or Dictionary. The JSONSerialization class has two methods, `JSONObjectWithData` and `JSONObjectWithStream`, that are used to deserialize JSON data. 

# Section 3: JSONObjectWithData

The `JSONObjectWithData` method takes an NSData object as an argument and returns an NSDictionary. This method is used to deserialize JSON data that is stored in an NSData object. 

# Section 4: JSONObjectWithStream

The `JSONObjectWithStream` method takes an NSInputStream object as an argument and returns an NSDictionary. This method is used to deserialize JSON data that is stored in an NSInputStream object.
