---
title: What is the difference between using file.separator and file.pathseparator?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: File.separator should be used to separate components of a file path, while File.pathSeparator should be used to separate paths in a list of paths.
---

**Contents**

[TOC]

### File.separator

File.separator is used to separate file paths in a system-independent way. It will use the correct directory separator for the platform it is running on, such as `/` for Unix-based systems, or `\` for Windows-based systems.

### File.pathSeparator

File.pathSeparator is used to separate multiple paths in a system-independent way. It will use the correct separator for the platform it is running on, such as `:` for Unix-based systems, or `;` for Windows-based systems.
