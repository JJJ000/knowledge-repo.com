---
title: Comparing the Maven parent project pom file to the Maven module project pom files
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: A parent pom is a pom.xml file that is used to manage the versions and dependencies of a group of related Maven modules, while a module pom is a pom.xml file that defines the configuration for a single Maven module.
---

**Contents**

[TOC]

### Maven Parent POM
Maven Parent POM is a special type of POM (Project Object Model) which is used to structure the project to maintain the consistency among all the modules or sub-projects. It is used to define the common configuration which is applicable to all the modules of the project. It is also used to configure the common plugins and dependencies.

### Modules POM
Modules POM is a type of POM (Project Object Model) which is used to define the specific configuration for a particular module of the project. It is used to configure the specific plugins and dependencies which are applicable to the particular module. It also inherits the configuration from the parent POM.
