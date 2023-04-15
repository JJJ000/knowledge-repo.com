---
title: Changing the default Java character encoding
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The default Java character encoding can be set by using the System.setProperty() method.
---

**Contents**

[TOC]

**1. Overview**

The default Java character encoding is used to convert bytes into characters when reading and writing text files. It is important to set the correct character encoding to ensure that text files are correctly interpreted.

**2. Locating the Default Character Encoding**

The default character encoding for Java can be found by using the System.getProperty("file.encoding") method. This will return the default character encoding for the platform.

**3. Setting the Default Character Encoding**

The default character encoding can be set by using the System.setProperty("file.encoding", "value") method. The value should be set to the desired character encoding.

**4. Example**

For example, to set the default character encoding to UTF-8, the following code can be used:

```
System.setProperty("file.encoding", "UTF-8");
```
