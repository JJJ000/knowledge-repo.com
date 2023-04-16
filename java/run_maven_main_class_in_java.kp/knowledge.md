---
title: Execute the main class of the Maven project
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Run the main class of a Maven project in Java by using the command `mvn execjava -Dexec.mainClass=<fully qualified class name>`.
---

**Contents**

[TOC]

## Step 1: Create a Maven Project

To create a Maven project, use the following command: 

`mvn archetype:generate -DgroupId=<group-id> -DartifactId=<artifact-id> -DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false`

## Step 2: Add Main Class

In the `src/main/java` directory, add the main class of your Maven project. The main class should have a `public static void main(String[] args)` method. 

## Step 3: Add Dependencies

If your project requires any additional dependencies, add them to the `pom.xml` file.

## Step 4: Run Main Class

To run the main class of your Maven project, use the following command:

`mvn exec:java -Dexec.mainClass="<fully-qualified-classname>"`
