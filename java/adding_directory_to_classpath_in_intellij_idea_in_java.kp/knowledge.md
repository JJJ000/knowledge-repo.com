---
title: What is the process for adding a directory to the classpath of an application run profile in intellij idea?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: In IntelliJ IDEA, you can add a directory to the classpath in an application run profile by selecting the directory in the Classpath tab of the Edit Configuration window.
---

**Contents**

[TOC]

# Section 1: Configuring IntelliJ IDEA
1. Open IntelliJ IDEA and select the project for which you want to add the directory to the classpath.
2. Click on the File menu and select Project Structure.
3. Select the Modules option from the left-hand side panel.
4. Select the Dependencies tab and click on the + button to add a new dependency.
5. Select JARs or directories and select the directory that you want to add to the classpath.

# Section 2: Setting the Classpath
1. Open the Run/Debug Configurations window by clicking on the Run menu and selecting Edit Configurations.
2. Select the application run profile for which you want to set the classpath.
3. Click on the Environment Variables button and add a new variable with the name CLASSPATH and the value of the directory that you want to add to the classpath.

# Section 3: Verifying the Classpath
1. Open a terminal window and go to the project directory.
2. Run the command `echo $CLASSPATH` to verify that the directory has been added to the classpath.

# Section 4: Running the Application
1. Run the application using the application run profile that you configured in the previous step.
2. Verify that the application is running correctly and that the directory has been added to the classpath.
