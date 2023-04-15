---
title: Combining two JSON files utilizing jackson
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Merging two JSON documents using Jackson in Java involves parsing the JSON files to create two separate Object nodes, then recursively merging each field from one node into the other.
---

**Contents**

[TOC]

## Introduction
JSON (JavaScript Object Notation) is a lightweight and easy-to-read format for data exchange. In certain cases, it may be necessary to combine or merge two JSON documents. Fortunately, the Jackson library provides a simple and efficient solution to this problem in Java.

This tutorial will guide you through the steps to merge two JSON documents using Jackson in Java.

## Step 1: Creating JSON documents

Before we can merge two JSON documents, we need to create them first. For this purpose, we will create two JSON files, `json1.json` and `json2.json`, each with different data.

```json
// json1.json
{
  "name": "John Doe",
  "age": 30,
  "address": {
    "street": "123 Main St",
    "city": "Anytown",
    "state": "CA"
  }
}
```

```json
// json2.json
{
  "name": "Jane Doe",
  "email": "jane.doe@example.com",
  "address": {
    "street": "456 Oak Ave",
    "city": "Anytown",
    "state": "CA",
    "zip": "12345"
  }
}
```

## Step 2: Reading JSON documents

Once we have our JSON documents, we need to read them using Jackson's `ObjectMapper` class.

```java
// Read json1.json into a JsonNode object
JsonNode json1 = new ObjectMapper().readTree(new File("json1.json"));

// Read json2.json into a JsonNode object
JsonNode json2 = new ObjectMapper().readTree(new File("json2.json"));
```

The `readTree` method returns a `JsonNode` object which represents the JSON document.

## Step 3: Merging JSON documents

To merge the two JSON documents, we can use the `ObjectNode` class from the Jackson library. This class extends `JsonNode` and provides additional methods for editing JSON objects. We will create an `ObjectNode` object by copying the contents of the first JSON document and then use the `setAll` method to add the contents of the second JSON document.

```java
// Create an ObjectNode object with the contents of json1
ObjectNode merged = (ObjectNode) json1.deepCopy();

// Merge json2 into merged ObjectNode
merged.setAll((ObjectNode) json2);
```

The `deepCopy` method creates a copy of the JSON document to prevent any unwanted side effects to the original document.

## Step 4: Writing the merged document

Finally, we can write the merged JSON document to a file or print it to the console using Jackson's `ObjectMapper` class.

```java
// Write merged JSON document to a file
new ObjectMapper().writeValue(new File("merged.json"), merged);

// Print merged JSON document to console
System.out.println(merged.toPrettyString());
```

The `writeValue` method writes the `ObjectNode` object to a JSON file, while the `toPrettyString` method converts the `ObjectNode` object to a formatted JSON string for printing to the console.

## Conclusion
In this tutorial, we learned how to merge two JSON documents using Jackson in Java. We accomplished this by creating `ObjectNode` objects from the JSON documents, merging them using the `setAll` method, and writing the resulting JSON document to a file or printing it to the console. Jackson provides a robust and efficient solution for working with JSON data in Java.
