---
title: Automatically generate the full directory when creating a new file
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The Files.createDirectories() method can be used to create the entire path to a new file automatically in Java.
---

**Contents**

[TOC]

# Creating the File

The first step in creating a new file in Java is to create a `File` object. This object will represent the file that is to be written to. The `File` constructor takes a single argument, which is the path of the file to be created. 

For example, the following code creates a `File` object for a file located at `/Users/user/Documents/example.txt`:

```java
File file = new File("/Users/user/Documents/example.txt");
```

# Creating the Path

The second step is to create the path of the file if it does not already exist. This can be done by calling the `mkdirs()` method on the `File` object. This method will create all of the necessary directories in the path in order to create the file.

For example, the following code creates the path of the `File` object created in the previous step:

```java
file.mkdirs();
```

# Writing to the File

The third step is to write to the file. This can be done by using the `FileWriter` class, which provides methods for writing to a file. The `FileWriter` constructor takes a single argument, which is the `File` object that was created in the first step.

For example, the following code creates a `FileWriter` object and writes a string to the file:

```java
FileWriter writer = new FileWriter(file);
writer.write("This is an example string.");
writer.close();
```

# Closing the File

The fourth and final step is to close the file after it has been written to. This can be done by calling the `close()` method on the `FileWriter` object. This will ensure that all of the data is written to the file and that the file is properly closed.

For example, the following code closes the `FileWriter` object created in the previous step:

```java
writer.close();
```
