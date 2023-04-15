---
title: What is the process for making a directory in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To create a directory in Java, use the File.mkdir() or File.mkdirs() method.
---

**Contents**

[TOC]

1. **Import Necessary Packages**
    ```java
    import java.io.File;
    ```

2. **Create a File Object**
    ```java
    File directory = new File("DirectoryName");
    ```

3. **Create the Directory**
    ```java
    directory.mkdir();
    ```

4. **Check if Directory was Created**
    ```java
    if (directory.exists()) {
        System.out.println("Directory created successfully");
    } else {
        System.out.println("Failed to create directory");
    }
    ```
