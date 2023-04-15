---
title: What makes final variables accessible in anonymous classes?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Anonymous classes do not have a name, so they cannot access non-final variables due to the restriction of variable access within inner classes.
---

**Contents**

[TOC]

### Accessibility of Final Variables
In anonymous classes, variables that are declared as `final` can be accessed. This is because anonymous classes do not have a name and are defined within a method, so the variables must be `final` in order to be accessed.

### Benefits of Final Variables
Using `final` variables in anonymous classes provides several benefits. First, it ensures that the variable is immutable and cannot be changed, which can help prevent errors. Additionally, it helps improve the readability of the code by making it clear that the variable is not going to be modified.

### Limitations of Final Variables
The use of `final` variables in anonymous classes also has some limitations. Since the variables are not modifiable, they cannot be used to store data that needs to be updated. Additionally, the variables must be declared and initialized before the anonymous class is declared, which can lead to code that is difficult to read and maintain.

### Conclusion
Using `final` variables in anonymous classes can provide several benefits, such as ensuring that the variable is immutable and improving the readability of the code. However, there are also some limitations, such as the inability to store data that needs to be updated and the need to declare and initialize the variable before the anonymous class is declared.
