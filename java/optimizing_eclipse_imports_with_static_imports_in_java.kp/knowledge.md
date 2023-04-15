---
title: Optimize eclipse to include static imports using the 'optimize imports' feature
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Yes, Eclipse can optimize imports to include static imports in Java.
---

**Contents**

[TOC]

### What is Eclipse Optimize Imports?

Eclipse Optimize Imports is a feature of the Eclipse IDE that allows developers to quickly and easily organize and clean up the imports in their Java source code. It removes unused imports and organizes the remaining imports into alphabetical order. This can help developers quickly find the imports they need and make their code more readable.

### What are Static Imports?

Static imports are a way of importing static members from classes and interfaces. This allows developers to access static members directly without having to use the class name. Static imports can make code more concise and readable, since developers don't need to specify the class name each time they use a static member.

### How Does Eclipse Optimize Imports Handle Static Imports?

Eclipse Optimize Imports can be configured to include static imports in its analysis. When this option is enabled, Eclipse will check for unused static imports and will organize the remaining static imports in the same way as non-static imports. This allows developers to quickly find and organize their static imports as well.

### How to Enable Static Imports in Eclipse Optimize Imports

To enable static imports in Eclipse Optimize Imports, go to the Eclipse Preferences window, select Java -> Code Style -> Organize Imports and check the box labeled "Include static imports". This will enable Eclipse Optimize Imports to include static imports in its analysis.
