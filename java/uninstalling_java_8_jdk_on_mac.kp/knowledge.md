---
title: Uninstalling Java 8 jdk from mac
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Open the Terminal and run the command `sudo rm -rf /Library/Java/JavaVirtualMachines/jdk1.8.0\_*.jdk`.
---

**Contents**

[TOC]

### Uninstalling Java 8 JDK
1. Open the **Terminal** application.
2. Type `sudo rm -fr /Library/Java/JavaVirtualMachines/jdk1.8.0_191.jdk` and press **Enter**.
3. Type your user name and password when prompted and press **Enter**.

### Removing Java 8 JDK from the System Path
1. Open **Terminal**.
2. Type `sudo nano /etc/paths` and press **Enter**.
3. Remove the line containing the path to the JDK.
4. Press **Ctrl+O** to save the file and **Ctrl+X** to exit.
