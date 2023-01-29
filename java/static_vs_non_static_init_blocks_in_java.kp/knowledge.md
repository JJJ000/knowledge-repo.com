---
title: How do static and non-static initialization code blocks differ?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: A static initialization code block is executed once when the class is loaded, while a non-static initialization code block is executed each time an instance of the class is created.
---

**Contents**

[TOC]

1. **Static Initialization Code Block**
- A static initialization code block is a set of code that is used to initialize static fields of a class. This code is executed when the class is first loaded into memory. The static initialization code block is executed only once and is usually used to initialize static fields of a class.

2. **Non-Static Initialization Code Block**
- A non-static initialization code block is a set of code that is used to initialize non-static fields of a class. This code is executed every time an instance of the class is created. The non-static initialization code block is executed each time an instance of the class is created and is usually used to initialize non-static fields of a class.
