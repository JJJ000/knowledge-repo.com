---
title: Create a JSON string from an nsdictionary in ios
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: You can generate a JSON string from an NSDictionary in iOS by using the NSJSONSerialization class.
---

**Contents**

[TOC]

## Section 1: Parsing the NSDictionary

The first step to generating a JSON string from an NSDictionary is to parse the NSDictionary. This can be done using the `NSJSONSerialization` class. This class provides methods for converting a Foundation object into JSON data. To parse the NSDictionary, you can use the `dataWithJSONObject:options:error:` method, which takes the NSDictionary object and an optional set of serialization options as parameters.

## Section 2: Generating the JSON String

Once the NSDictionary has been parsed, the next step is to generate the JSON string. This can be done using the `NSJSONSerialization` class again, this time using the `JSONObjectWithData:options:error:` method. This method takes the parsed NSDictionary data and an optional set of deserialization options as parameters, and returns an NSString containing the JSON string.

## Section 3: Formatting the JSON String

The final step is to format the JSON string. This can be done using the `NSJSONSerialization` class again, this time using the `stringWithJSONObject:options:error:` method. This method takes the parsed NSDictionary data and an optional set of formatting options as parameters, and returns an NSString containing the formatted JSON string.

## Section 4: Writing the JSON String to a File

Once the JSON string has been generated and formatted, it can be written to a file. This can be done using the `NSFileManager` class, which provides methods for writing and reading files. To write the JSON string to a file, you can use the `writeData:toFile:atomically:` method, which takes the JSON data and the path of the file to write to as parameters.
