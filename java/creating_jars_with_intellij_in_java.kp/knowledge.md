---
title: What is the correct way to create jars using intellij?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To build JARs from IntelliJ properly in Java, use the `Build > Build Artifacts` menu option.
---

**Contents**

[TOC]

### Prerequisites
Before you can build a JAR from IntelliJ, you must have the following: 
- IntelliJ installed 
- JDK installed 
- A project in IntelliJ with the source code 

### Setting up the Project
1. Open the project in IntelliJ.
2. Select "File > Project Structure" from the menu.
3. Select "Artifacts" from the left sidebar.
4. Click the "+" button, and select "JAR > From modules with dependencies".
5. Select the main class of your project.
6. Select the appropriate JAR files to include.
7. Click "OK".

### Building the JAR
1. Select "Build > Build Artifacts" from the menu.
2. Select the artifact you created in the previous step.
3. Click "Build".

### Running the JAR
1. Open a terminal window and navigate to the directory where the JAR was built.
2. Run the JAR with the command "java -jar <name_of_jar>.jar".
