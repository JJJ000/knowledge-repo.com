---
title: What is the process for using nsjsonserialization?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: NSJSONSerialization is used to convert JSON data into Foundation objects and convert Foundation objects into JSON data.
---

**Contents**

[TOC]

## Section 1: Import NSJSONSerialization

In order to use NSJSONSerialization, you must first import the framework. To do this, add the following line of code to the top of your file:

```
import Foundation
```

## Section 2: Create a JSON Object

Once you have imported the NSJSONSerialization framework, you can create a JSON object by passing in a valid JSON string. For example:

```
let jsonString = "{\"name\":\"John\",\"age\":30}"
let jsonData = jsonString.data(using: .utf8)!
let jsonObject = try? JSONSerialization.jsonObject(with: jsonData, options: [])
```

## Section 3: Access JSON Data

Once you have created a JSON object, you can access its data by casting it as a Dictionary or Array. For example:

```
if let jsonDict = jsonObject as? [String: Any] {
    let name = jsonDict["name"] as? String
    let age = jsonDict["age"] as? Int
}
```

## Section 4: Convert JSON Object to Data

You can also convert a JSON object back to data by using the `JSONSerialization.data()` method. For example:

```
let jsonData = try? JSONSerialization.data(withJSONObject: jsonObject, options: [])
```
