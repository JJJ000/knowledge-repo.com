---
title: What is the process for installing jdk 11 on ubuntu?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Run `sudo apt install openjdk-11-jdk` in the terminal to install JDK 11 under Ubuntu.
---

**Contents**

[TOC]

# Section 1: Download JDK 11
1. Go to the [Oracle JDK 11 download page](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. Select the appropriate version for your system.
3. Accept the license agreement and download the tar.gz file.

# Section 2: Install JDK 11
1. Open the terminal and navigate to the directory where the tar.gz file is downloaded.
2. Unzip the file using the command `tar -xvzf <filename>`.
3. Move the extracted folder to `/usr/lib/jvm` using the command `sudo mv <folder_name> /usr/lib/jvm`.

# Section 3: Set Environment Variables
1. Set the `JAVA_HOME` environment variable using the command `sudo nano /etc/environment`.
2. Add the following line to the file `JAVA_HOME="/usr/lib/jvm/<folder_name>"`.
3. Save the file and exit.

# Section 4: Verify Installation
1. Execute the command `java -version` to verify the installation.
2. The output should display the version of the JDK installed.
