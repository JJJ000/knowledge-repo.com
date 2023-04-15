---
title: What is the process for adding the javax.servlet / jakarta.servlet API to my eclipse project?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Right-click on the project in Eclipse and select `Build Path > Add Libraries > Server Runtime > Apache Tomcat`.
---

**Contents**

[TOC]

### Download the Library
1. Download the jakarta.servlet-api library from the [Maven Central Repository](https://search.maven.org/search?q=g:jakarta.servlet%20AND%20a:jakarta.servlet-api).
2. Extract the .jar file from the downloaded .zip file.

### Add the Library to the Build Path
1. Right-click on the project in the Eclipse Package Explorer.
2. Select Build Path > Configure Build Path.
3. Select the Libraries tab.
4. Click Add External JARs...
5. Select the jakarta.servlet-api.jar file.
6. Click OK.

### Add the Library to the Deployment Assembly
1. Right-click on the project in the Eclipse Package Explorer.
2. Select Properties.
3. Select Deployment Assembly.
4. Click Add...
5. Select Java Build Path Entries.
6. Select jakarta.servlet-api.jar.
7. Click Finish.

### Verify the Library
1. Right-click on the project in the Eclipse Package Explorer.
2. Select Properties.
3. Select Java Build Path.
4. Select the Libraries tab.
5. Verify that the jakarta.servlet-api library is listed.
