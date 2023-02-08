---
title: Should I make jackson's objectmapper a static field?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: No, it is best to create a new ObjectMapper instance each time it is needed.
---

**Contents**

[TOC]

1. Advantages of Declaring Jackson's ObjectMapper as a Static Field
- Reusability: Declaring a static ObjectMapper field allows for the same instance to be used throughout the application, which can be more efficient than creating a new instance every time.
- Thread-safety: A static ObjectMapper is thread-safe, meaning that multiple threads can use the same instance without any issues.

2. Disadvantages of Declaring Jackson's ObjectMapper as a Static Field
- Memory Usage: A static ObjectMapper field will take up more memory than creating a new instance every time, as it is stored in memory for the entire duration of the application.
- Configuration: If the ObjectMapper needs to be configured differently for different parts of the application, a static ObjectMapper field may not be the best solution, as it will have to be configured once and used throughout the application.
