---
title: Add Maven dependencies to intellij idea
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: In IntelliJ IDEA, dependencies can be imported from a Maven project by selecting File > Project Structure > Modules > Dependencies tab and clicking the `+` icon.
---

**Contents**

[TOC]

## Step 1: Add Dependencies to pom.xml

To add dependencies to your project, you must first add the dependencies to the pom.xml file. This can be done by adding the following code to the pom.xml file:

```
<dependency>
    <groupId>groupId</groupId>
    <artifactId>artifactId</artifactId>
    <version>version</version>
</dependency>
```

Where `groupId`, `artifactId` and `version` are the coordinates of the dependency you want to add.

## Step 2: Import Dependencies

Once the dependencies have been added to the pom.xml file, you can import them into your project in IntelliJ IDEA by selecting the `File` menu, then selecting `Project Structure`, and then selecting the `Modules` tab.

In the `Modules` tab, select your project, then select the `Dependencies` tab. Finally, select the `+` button, and choose `Import Maven Projects`.

## Step 3: Select Dependencies

In the `Import Maven Projects` window, select the dependencies you want to import, and then click `OK`. The dependencies will be imported into your project.

## Step 4: Refresh Dependencies

Finally, you must refresh the dependencies in IntelliJ IDEA by selecting the `Maven` menu, then selecting `Reimport`. This will update the project with the newly imported dependencies.
