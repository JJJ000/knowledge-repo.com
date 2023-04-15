---
title: Error a subclass must implement the method from its superclass
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To fix this error, you must either implement the abstract method in the subclass or mark the subclass as abstract.
---

**Contents**

[TOC]

### Solution 1:
If you have imported a project into Eclipse and are getting a 'Must Override a Superclass Method' error, the first thing you should do is check the Java compiler compliance level. To do this, go to `Project > Properties > Java Compiler` and make sure that the Compiler compliance level is set to the same version of Java as the project.

### Solution 2:
If the compiler compliance level is set correctly, then the next step is to check the project's build path. To do this, go to `Project > Properties > Java Build Path` and make sure that all of the libraries and dependencies are set up correctly.

### Solution 3:
If the build path is correct, then the next step is to check the project's source code. Look for any methods that are not properly overriding superclass methods. If you find any, make sure to fix them so that they are properly overriding the superclass methods.

### Solution 4:
Finally, if all of the above steps have been completed and the error is still occurring, it may be necessary to clean and rebuild the project. To do this, go to `Project > Clean` and then select the project you want to clean. After this, you can then go to `Project > Build All` to rebuild the project.
