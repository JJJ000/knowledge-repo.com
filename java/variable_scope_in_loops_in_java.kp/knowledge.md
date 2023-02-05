---
title: Assigning values to variables within or outside of a loop
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Generally, it is best practice to declare variables outside of a loop in Java.
---

**Contents**

[TOC]

# Inside a Loop

Variables declared inside a loop are known as local variables. These variables are only accessible within the loop, and once the loop is exited, the variables are destroyed. Local variables are declared using the same syntax as any other variable declaration.

# Outside a Loop

Variables declared outside of a loop are known as global variables. These variables are accessible from anywhere in the code and are not destroyed when the loop is exited. Global variables are declared using the same syntax as any other variable declaration.
