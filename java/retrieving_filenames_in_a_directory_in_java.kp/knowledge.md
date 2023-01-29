---
title: Retrieving the names of all files in a directory
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the Files.walk() method to get the filenames of all files in a folder in Java.
---

**Contents**

[TOC]

### Using File Class
The File class provides methods to get the list of all the files in a folder.

### Syntax
```
File folder = new File(directoryPath);
File[] listOfFiles = folder.listFiles();
```

### Example
```
public static void main(String[] args) {
    String directoryPath = "C:/Users/user/Documents/";
    File folder = new File(directoryPath);
    File[] listOfFiles = folder.listFiles();

    for (File file : listOfFiles) {
        if (file.isFile()) {
            System.out.println(file.getName());
        }
    }
}
```

### Using Files Class
The Files class provides methods to get the list of all the files in a folder.

### Syntax
```
Path directoryPath = Paths.get(directoryPath);
Stream<Path> streamOfPaths = Files.list(directoryPath);
```

### Example
```
public static void main(String[] args) {
    String directoryPath = "C:/Users/user/Documents/";
    Path directoryPath = Paths.get(directoryPath);
    Stream<Path> streamOfPaths = Files.list(directoryPath);

    streamOfPaths.forEach(System.out::println);
}
```
