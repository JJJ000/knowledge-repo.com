---
title: What command do I use to set gradle to a specific jdk version?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: In the `build.gradle` file, set the `sourceCompatibility` and `targetCompatibility` properties to the desired JDK version.
---

**Contents**

[TOC]

### Setting the JDK Path in Gradle

1. Open the `gradle.properties` file located in the root of your project.
2. Add the following line to the file: `org.gradle.java.home=<path_to_jdk>`
3. Replace `<path_to_jdk>` with the absolute path to the JDK directory.

### Configuring the JDK Version in Gradle

1. Open the `build.gradle` file located in the root of your project.
2. Add the following line to the file: `sourceCompatibility = "<jdk_version>"`
3. Replace `<jdk_version>` with the JDK version you want to use.

### Testing the JDK Version

1. Run the following command in the terminal: `./gradlew tasks`
2. If the command was successful, the output should include a line specifying the JDK version you set.

### Troubleshooting

If the command does not show the correct JDK version, double-check that you have set the correct path in the `gradle.properties` file and the correct version in the `build.gradle` file. If the issue persists, make sure you have installed the correct JDK version.
