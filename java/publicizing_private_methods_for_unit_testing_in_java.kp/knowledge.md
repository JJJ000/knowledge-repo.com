---
title: Is it a good idea to make a private method public in order to unit test it?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Yes, it is a good idea to make a private method public in Java in order to unit test it.
---

**Contents**

[TOC]

### Pros

Making a private method public to unit test it can be beneficial in Java, as it allows the method to be tested more thoroughly. This can help to ensure that the code is functioning as expected, and can be a useful tool for debugging.

### Cons

Making a private method public can also have some drawbacks, as it can lead to code that is less secure and more prone to errors. It can also lead to a decrease in code maintainability, as the code becomes more complex and difficult to read. Additionally, it can lead to code that is more difficult to debug, as it can be harder to identify the source of any potential issues.

### Alternatives

An alternative to making a private method public to unit test it is to use reflection. Reflection allows code to access and modify private fields and methods, and can be used to test private methods without making them public. This can help to keep code secure and maintainable, while still allowing for thorough testing.
