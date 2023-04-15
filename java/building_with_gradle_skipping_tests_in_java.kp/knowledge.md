---
title: Build gradle without running tests
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To build a Gradle project without tests in Java, run the command `gradle build -x test`.
---

**Contents**

[TOC]

### Gradle Build without Tests

### Step 1: Create a New Project

Create a new Java project in your preferred IDE or text editor. Make sure to include the necessary Gradle files, such as `build.gradle` and `settings.gradle`.

### Step 2: Configure Gradle

Open the `build.gradle` file and add the following lines to configure the project for Gradle:

```java
apply plugin: 'java'

sourceCompatibility = 1.8

repositories {
    mavenCentral()
}

dependencies {
    testCompile group: 'junit', name: 'junit', version: '4.12'
}
```

### Step 3: Exclude Tests

Add the following line to the `build.gradle` file to exclude tests from the build:

```java
test {
    exclude '**/*Test.java'
}
```

### Step 4: Build the Project

Run the `gradle build` command to build the project without running any tests.
