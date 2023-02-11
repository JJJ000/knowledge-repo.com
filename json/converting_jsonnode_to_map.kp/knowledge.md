---
title: Transform a jsonnode object into a map
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: The Jackson library can be used to convert a JsonNode object to a Map.
---

**Contents**

[TOC]

##### Section 1: Using ObjectMapper

The most straightforward way to convert a `JsonNode` object to a `Map` is to use the `ObjectMapper` class from the Jackson library. This class provides a `convertValue` method which can be used to convert a `JsonNode` object to a `Map`:

```java
ObjectMapper mapper = new ObjectMapper();
Map<String, Object> map = mapper.convertValue(jsonNode, Map.class);
```

##### Section 2: Using TreeTraversingParser

Another way to convert a `JsonNode` object to a `Map` is to use the `TreeTraversingParser` class from the Jackson library. This class provides a `readValueAsTree` method which can be used to convert a `JsonNode` object to a `Map`:

```java
TreeTraversingParser parser = new TreeTraversingParser(jsonNode);
Map<String, Object> map = parser.readValueAsTree();
```

##### Section 3: Using Stream API

It is also possible to convert a `JsonNode` object to a `Map` using the Java 8 Stream API. This can be done by iterating over the `JsonNode` object and mapping each key-value pair to a `Map` entry:

```java
Map<String, Object> map = jsonNode.fields().collect(Collectors.toMap(
    Map.Entry::getKey,
    Map.Entry::getValue
));
```

##### Section 4: Using Iterator

Finally, it is possible to convert a `JsonNode` object to a `Map` using an `Iterator`:

```java
Iterator<Map.Entry<String, JsonNode>> it = jsonNode.fields();
Map<String, Object> map = new HashMap<>();
while (it.hasNext()) {
    Map.Entry<String, JsonNode> entry = it.next();
    map.put(entry.getKey(), entry.getValue());
}
```
