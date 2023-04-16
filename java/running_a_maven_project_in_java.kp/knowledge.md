---
title: Launch a Maven project
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To run a Maven project in Java, use the `mvn clean install` command.
---

**Contents**

[TOC]

# Section 1: Prerequisites

Before running a Maven project in Java, there are a few prerequisites that must be met: 

- Java Development Kit (JDK) must be installed and configured correctly. 
- Apache Maven must be installed and configured correctly.
- The project must be configured with a valid pom.xml file.

# Section 2: Setup

Once the prerequisites are met, the project can be set up to run with Maven. This can be done by running the following command in the project’s root directory: 

`mvn install`

This will install all the dependencies required for the project, and create the necessary files and directories. 

# Section 3: Compile and Execute

Once the project is set up, it can be compiled and executed using the following command:

`mvn compile exec:java`

This command will compile the project and execute the main class.

# Section 4: Troubleshooting

If the project fails to compile or execute, it is likely that there is an issue with the configuration or dependencies. In this case, it is recommended to check the pom.xml file and ensure that all dependencies are correct. Additionally, it is possible to run the project in debug mode to help identify the cause of any errors.
