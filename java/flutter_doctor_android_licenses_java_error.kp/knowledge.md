---
title: Running 'flutter doctor --android-licenses' results in a Java error
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The Java error is likely due to a missing or outdated Java Development Kit (JDK).
---

**Contents**

[TOC]

### Solution

### Step 1: Check Java Version
First, check if you have the correct version of Java installed. You should have Java 8 or higher for Android development.

### Step 2: Set Environment Variables
Next, you need to set the environment variables for Java. This involves setting the JAVA_HOME environment variable to the location of the Java installation.

### Step 3: Accept Licenses
Finally, you need to accept the Android SDK licenses. To do this, run the command `flutter doctor --android-licenses` and accept the licenses when prompted.
