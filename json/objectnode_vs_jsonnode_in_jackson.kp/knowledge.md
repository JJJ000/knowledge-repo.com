---
title: How do objectnode and jsonnode in Jackson differ?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-14 00:00:00
updated_at: 2023-02-14 00:00:00
tldr: ObjectNode is an implementation of JsonNode that allows for direct manipulation of the underlying JSON object.
---

**Contents**

[TOC]

#ObjectNode
ObjectNode is a type of node that is used to represent a JSON object. It is a subtype of JsonNode and provides methods to add, remove and modify fields of the JSON object.

#JsonNode
JsonNode is a type of node that is used to represent a JSON tree. It is an abstract class that provides methods to access and modify the data in the tree. It can also be used to traverse the tree and query the data.

#Differences
1. ObjectNode is used to represent a JSON object whereas JsonNode is used to represent a JSON tree.
2. ObjectNode provides methods to add, remove and modify fields of the JSON object whereas JsonNode provides methods to access and modify the data in the tree.
3. ObjectNode is a subtype of JsonNode.
