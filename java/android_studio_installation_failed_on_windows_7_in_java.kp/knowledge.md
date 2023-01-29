---
title: The installation of Android studio on windows 7 is unsuccessful due to the lack of a jdk
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The installation may be failing due to a missing JDK in the system`s Java installation.
---

**Contents**

[TOC]

### Prerequisites 
1. Java Development Kit (JDK) 8 or higher
2. Android Studio

### Installation Steps
1. Download and install the latest JDK from the [Oracle website](https://www.oracle.com/java/technologies/javase-downloads.html).
2. Download and install Android Studio from the [Android website](https://developer.android.com/studio).
3. Follow the on-screen instructions to complete the installation.

### Troubleshooting
1. If the installation fails with an error saying "No JDK found in Java", it means that the JDK is not installed or is not configured correctly.
2. Check if the JDK is installed and configured correctly by running `java -version` in the command prompt.
3. If the command returns an error, then the JDK is not installed or configured correctly.
4. Reinstall the JDK and configure it correctly. Refer to the [Oracle website](https://www.oracle.com/java/technologies/javase-downloads.html) for more information.
5. After the JDK is installed and configured correctly, try installing Android Studio again.
