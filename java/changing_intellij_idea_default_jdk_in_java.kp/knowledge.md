---
title: What is the process for altering the default jdk in intellij idea?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Go to File > Project Structure > Platform Settings > SDKs to change the IntelliJ IDEA default JDK.
---

**Contents**

[TOC]

# Section 1 - Locating the JDK
1. Open IntelliJ IDEA.
2. Select **File** > **Project Structure**.
3. Select **Platform Settings** > **SDKs**.

# Section 2 - Adding the JDK
1. Click the **+** icon.
2. Select **JDK**.
3. Navigate to the location of the JDK and select it.

# Section 3 - Setting the JDK as Default
1. Select the JDK that was just added.
2. Click the **Make Default** button.

# Section 4 - Verifying the Default JDK
1. Select **File** > **Project Structure**.
2. Select **Platform Settings** > **SDKs**.
3. Verify that the desired JDK is marked as **Default**.
