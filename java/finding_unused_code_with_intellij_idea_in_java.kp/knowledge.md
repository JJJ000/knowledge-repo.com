---
title: What is the process for locating all unused code in intellij idea?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: In IntelliJ IDEA, you can use the `Code | Optimize Imports` command to find unused code in Java.
---

**Contents**

[TOC]

### Setting up IntelliJ
1. Open your project in IntelliJ.
2. Navigate to `Analyze` > `Inspect Code...`
3. Select the scope of the inspection. You can choose to inspect the whole project or just the files you are interested in.

### Selecting Inspection Profile
1. Choose the inspection profile you want to use. IntelliJ comes with several pre-made profiles, such as `Default`, `Android`, `Java`, and more.
2. Click `OK`.

### Running the Inspection
1. Click `Run` to start the inspection.
2. IntelliJ will now analyze the code and display any unused code.

### Viewing Results
1. In the `Inspection Results` window, you can view the results of the inspection.
2. Unused code is highlighted in yellow.
3. You can click on any of the highlighted code to see more information about why it is unused.
