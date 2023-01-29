---
title: Increasing the version numbers of the components in a multi-module Maven project
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The version numbers of modules in a multi-module Maven project can be updated by modifying the <version> tag in the project`s pom.xml file.
---

**Contents**

[TOC]

### Update the Version Number

The version number of a module in a multi-module Maven project in Java can be updated by editing the version number in the `pom.xml` file. The version number is located in the `<version>` tag under the `<project>` tag.

### Run the Maven Version Plugin

Once the version number is updated, the Maven Version Plugin must be run to ensure that all other modules in the project are updated with the new version number. The Maven Version Plugin can be run using the following command:

```java
mvn versions:set -DnewVersion=<new_version_number>
```

### Commit the Changes

After running the Maven Version Plugin, the changes must be committed to the version control system. This ensures that all other developers who are working on the project are aware of the version number change.

### Deploy the Changes

Finally, the changes must be deployed to the production environment. This can be done by running the `mvn deploy` command. This will ensure that all users of the application are aware of the new version number.
