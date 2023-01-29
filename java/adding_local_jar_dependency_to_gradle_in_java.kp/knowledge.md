---
title: What is the process for including a local .jar file as a dependency in a build.gradle file?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Add the .jar file to the `dependencies` section of the build.gradle file using the `compile files()` directive.
---

**Contents**

[TOC]

### Add the .jar File to the Project

1. Copy the .jar file into the `/libs` folder of your project.
2. Refresh the project in your IDE.

### Add the Dependency to the `build.gradle` File

1. Open the `build.gradle` file for your project.
2. Add the following line to the `dependencies` block:

```java
compile files('libs/<name-of-jar-file>.jar')
```

### Sync Gradle

1. Sync your Gradle project in your IDE.
2. Ensure that the .jar file is correctly included in the project.

### Use the Dependency

1. Import the classes from the .jar file into your project.
2. Use the classes as needed in your project.
