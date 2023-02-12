---
title: What is the process for adding new nodes to a jsonnode?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: Use the `put` method to create and insert new nodes in a JsonNode.
---

**Contents**

[TOC]

## Section 1: Create a JsonNode

Creating a JsonNode is done by using the JsonNode class from the Jackson library. To create a JsonNode, you must first create a Jackson ObjectMapper instance, which is used to create the JsonNode.

```
ObjectMapper mapper = new ObjectMapper();
```

Once the ObjectMapper is created, you can create a JsonNode by passing in a String, a File, or an InputStream.

## Section 2: Insert New Nodes

Once the JsonNode is created, you can insert new nodes into the tree using the set() method. The set() method takes two parameters: the path to the node and the value of the node.

For example, if you want to insert a new node with the key “name” and the value “John”, you can use the following code:

```
node.set("name", "John");
```

## Section 3: Nested Nodes

You can also insert nested nodes using the set() method. To do this, you must specify the full path to the node you want to insert. For example, if you want to insert a new node with the key “address” and the value “123 Main Street”, you can use the following code:

```
node.set("address.street", "123 Main Street");
```

## Section 4: Array Nodes

You can also insert nodes into an array using the set() method. To do this, you must specify the index of the array you want to insert the node into. For example, if you want to insert a new node with the key “name” and the value “John” into the first position of an array, you can use the following code:

```
node.set("array[0].name", "John");
```
