---
title: Recursively remove directories in java
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: To delete directories recursively in Java, use the Files.walkFileTree() method with a SimpleFileVisitor and the Files.delete() method.
---

**Contents**

[TOC]

### Using Apache Commons IO

Apache Commons IO provides a number of utility methods for deleting files and directories. The `FileUtils.deleteDirectory()` method can be used to delete a directory and all of its contents recursively.

Example:

```java
import org.apache.commons.io.FileUtils;

File directory = new File("/path/to/directory");
FileUtils.deleteDirectory(directory);
```

### Using Files

The `Files.walkFileTree()` method can be used to traverse a directory tree and delete each file and directory.

Example:

```java
import java.nio.file.Files;
import java.nio.file.Path;
import java.nio.file.Paths;

Path directory = Paths.get("/path/to/directory");
Files.walkFileTree(directory, new SimpleFileVisitor<Path>() {
    @Override
    public FileVisitResult visitFile(Path file, BasicFileAttributes attrs) throws IOException {
        Files.delete(file);
        return FileVisitResult.CONTINUE;
    }
    
    @Override
    public FileVisitResult postVisitDirectory(Path dir, IOException exc) throws IOException {
        Files.delete(dir);
        return FileVisitResult.CONTINUE;
    }
});
```

### Using Java 8 Streams

Java 8 Streams can be used to filter and delete files and directories in a single operation.

Example:

```java
import java.io.IOException;
import java.nio.file.Files;
import java.nio.file.Path;
import java.nio.file.Paths;

Path directory = Paths.get("/path/to/directory");
try {
    Files.walk(directory)
        .sorted(Comparator.reverseOrder())
        .map(Path::toFile)
        .forEach(File::delete);
} catch (IOException e) {
    e.printStackTrace();
}
```
