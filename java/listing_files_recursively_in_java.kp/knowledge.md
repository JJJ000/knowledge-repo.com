---
title: List files in Java using recursion
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: In Java, files can be listed recursively using the Files.walk() or Files.find() methods.
---

**Contents**

[TOC]

**1. Using Files.walk()**

Files.walk() is a utility method which recursively traverses a given directory and its subdirectories. It returns a Stream of Path objects for each file in the directory tree.

Syntax:

```
Files.walk(Path start, int maxDepth, FileVisitOption... options)
```

Example:

```
Path start = Paths.get("/home/user/Documents");
try (Stream<Path> stream = Files.walk(start, Integer.MAX_VALUE)) {
    stream.forEach(System.out::println);
} catch (IOException e) {
    e.printStackTrace();
}
```

**2. Using File.listFiles()**

File.listFiles() is a method which returns an array of File objects for all the files and directories in the directory. It can be used to recursively list files in a directory tree.

Syntax:

```
File[] listFiles(FileFilter filter)
```

Example:

```
File dir = new File("/home/user/Documents");
File[] files = dir.listFiles(new FileFilter() {
    public boolean accept(File file) {
        return file.isDirectory();
    }
});
for (File file : files) {
    System.out.println(file.getAbsolutePath());
}
```

**3. Using FileVisitor Interface**

FileVisitor is an interface which provides a callback mechanism to traverse a file tree. It provides several methods which are called by the Files.walkFileTree() method while traversing the directory tree.

Syntax:

```
Files.walkFileTree(Path start, FileVisitor<? super Path> visitor)
```

Example:

```
Path start = Paths.get("/home/user/Documents");
try {
    Files.walkFileTree(start, new SimpleFileVisitor<Path>() {
        @Override
        public FileVisitResult visitFile(Path file, BasicFileAttributes attrs) throws IOException {
            System.out.println(file.toString());
            return FileVisitResult.CONTINUE;
        }
    });
} catch (IOException e) {
    e.printStackTrace();
}
```

**4. Using Apache Commons IO**

Apache Commons IO is a library which provides various utility methods for manipulating files and directories. It provides a method FileUtils.listFiles() which can be used to recursively list files in a directory tree.

Syntax:

```
Collection<File> listFiles(File directory, String[] extensions, boolean recursive)
```

Example:

```
File directory = new File("/home/user/Documents");
String[] extensions = new String[] { "txt" };
Collection<File> files = FileUtils.listFiles(directory, extensions, true);
for (File file : files) {
    System.out.println(file.getAbsolutePath());
}
```
