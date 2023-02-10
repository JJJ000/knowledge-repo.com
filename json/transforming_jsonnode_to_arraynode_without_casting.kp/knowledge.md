---
title: How can Jackson convert a jsonnode to an arraynode without typecasting?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use the `ArrayNode.setAll(JsonNode)` method.
---

**Contents**

[TOC]

##### Using ObjectMapper

The ObjectMapper class of Jackson library provides the method `convertValue()` to convert the JsonNode to any other type of node. In order to convert JsonNode to ArrayNode, we can use the following code:

```java
ObjectMapper mapper = new ObjectMapper();
JsonNode jsonNode = ...;
ArrayNode arrayNode = mapper.convertValue(jsonNode, ArrayNode.class);
```

##### Using Tree Model

The Tree Model of Jackson library provides the method `set()` to convert the JsonNode to any other type of node. In order to convert JsonNode to ArrayNode, we can use the following code:

```java
ObjectMapper mapper = new ObjectMapper();
JsonNode jsonNode = ...;
ArrayNode arrayNode = mapper.createArrayNode();
arrayNode.set(jsonNode);
```

##### Using Iterator

The Iterator of Jackson library provides the method `next()` to convert the JsonNode to any other type of node. In order to convert JsonNode to ArrayNode, we can use the following code:

```java
ObjectMapper mapper = new ObjectMapper();
JsonNode jsonNode = ...;
ArrayNode arrayNode = mapper.createArrayNode();
Iterator<JsonNode> elements = jsonNode.elements();
while (elements.hasNext()) {
    arrayNode.add(elements.next());
}
```

##### Using Stream

The Stream of Jackson library provides the method `forEach()` to convert the JsonNode to any other type of node. In order to convert JsonNode to ArrayNode, we can use the following code:

```java
ObjectMapper mapper = new ObjectMapper();
JsonNode jsonNode = ...;
ArrayNode arrayNode = mapper.createArrayNode();
jsonNode.stream().forEach(arrayNode::add);
```
