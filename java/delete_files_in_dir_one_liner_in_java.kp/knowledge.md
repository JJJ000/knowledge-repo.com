---
title: Remove all files from the directory (not including the directory itself) - single command
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Files.walk(Paths.get(`directory`)).map(PathtoFile).forEach(Filedelete);
---

**Contents**

[TOC]

**Solution 1 - Using FileVisitor**

```java
Files.walkFileTree(Paths.get("directoryPath"), new SimpleFileVisitor<Path>() {
    @Override
    public FileVisitResult visitFile(Path file, BasicFileAttributes attrs) throws IOException {
        Files.delete(file);
        return FileVisitResult.CONTINUE;
    }
});
```

**Solution 2 - Using FileUtils**

```java
FileUtils.cleanDirectory(new File("directoryPath"));
```

**Solution 3 - Using Stream API**

```java
Files.list(Paths.get("directoryPath"))
  .filter(path -> !Files.isDirectory(path))
  .forEach(path -> {
    try {
      Files.delete(path);
    } catch (IOException e) {
      e.printStackTrace();
    }
  });
```

**Solution 4 - Using NIO2 Path API**

```java
Files.list(Paths.get("directoryPath"))
  .filter(Files::isRegularFile)
  .forEach(path -> {
    try {
      Files.delete(path);
    } catch (IOException e) {
      e.printStackTrace();
    }
  });
```
