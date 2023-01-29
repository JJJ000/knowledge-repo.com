---
title: What is the process for determining the number of lines of Java code in intellij idea?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: In IntelliJ IDEA, the lines of Java code can be counted by using the `Statistics` tool in the `Analyze` menu.
---

**Contents**

[TOC]

### Setting Up
1. Open the project in IntelliJ IDEA.
2. Navigate to **Tools** > **Run Statistics**.

### Running the Count
1. Select the scope of the count:
    - Entire Project: counts all the Java files in the project.
    - Current File: counts only the currently active file.
    - Directory: counts all the Java files in the selected directory.
2. Click **Run**.

### Viewing the Results
1. The results of the count will be displayed in the **Run Statistics** window.
2. The window will show the number of lines, classes, files, and packages.

### Exporting the Results
1. Click the **Export** button.
2. Select the format for the exported file.
3. Choose a location to save the file.
4. Click **OK**.
