---
title: Printing JSON in an attractive format using Jackson 2.2's objectmapper
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: The ObjectMapper class provides the ability to enable pretty printing of JSON output.
---

**Contents**

[TOC]

### Step 1: Configure ObjectMapper

To enable pretty printing, we need to configure the ObjectMapper. We can do this by using the `enable(SerializationFeature.INDENT_OUTPUT)` method:

```java
ObjectMapper mapper = new ObjectMapper();
mapper.enable(SerializationFeature.INDENT_OUTPUT);
```

### Step 2: Generate JSON

We can then generate JSON from an object by using the `writeValueAsString` method:

```java
String jsonString = mapper.writeValueAsString(myObject);
```

### Step 3: Print JSON

We can then print the JSON string with the `System.out.println` method:

```java
System.out.println(jsonString);
```

### Step 4: Verify Output

Finally, we can verify that the output is properly formatted by viewing the printed output.
