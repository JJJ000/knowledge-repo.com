---
title: What are the necessary dependencies for using Jackson mapper?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-14 00:00:00
updated_at: 2023-02-14 00:00:00
tldr: The dependencies required for using Jackson mapper in Json are Jackson-databind and Jackson-annotations.
---

**Contents**

[TOC]

### Dependency

```xml
<dependency>
    <groupId>com.fasterxml.jackson.core</groupId>
    <artifactId>jackson-databind</artifactId>
    <version>2.9.9</version>
</dependency>
```

### Optional Dependencies

```xml
<dependency>
    <groupId>com.fasterxml.jackson.core</groupId>
    <artifactId>jackson-core</artifactId>
    <version>2.9.9</version>
</dependency>

<dependency>
    <groupId>com.fasterxml.jackson.core</groupId>
    <artifactId>jackson-annotations</artifactId>
    <version>2.9.9</version>
</dependency>
```

### Maven Repository

```xml
<repository>
    <id>central</id>
    <name>Maven Central Repository</name>
    <url>http://repo1.maven.org/maven2/</url>
</repository>
```
