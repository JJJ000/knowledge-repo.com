---
title: Changing the Maven name of the jar artifact
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: The final name of a Maven jar artifact can be controlled by setting the <finalName> parameter in the <build> element of the project`s pom.xml file.
---

**Contents**

[TOC]

# Section 1: Setting the Final Name of the Artifact

Maven allows the user to control the final name of the jar artifact through the use of the `finalName` parameter in the `build` section of the `pom.xml` file. The value of the `finalName` parameter should be a string that is the desired name of the final jar artifact.

# Section 2: Example

For example, if the desired name of the jar artifact is `my-project-1.0.0.jar`, then the `finalName` parameter should be set to `my-project-1.0.0` in the `pom.xml` file:

```xml
<build>
  <finalName>my-project-1.0.0</finalName>
</build>
```

# Section 3: Effects

Setting the `finalName` parameter will affect the name of the jar artifact that is generated when the `mvn package` command is run. The final jar artifact will have the name specified in the `finalName` parameter.

# Section 4: Alternative

An alternative way to control the final name of the jar artifact is to use the `outputDirectory` and `finalName` parameters in the `build` section of the `pom.xml` file. The `outputDirectory` parameter should be set to the desired directory where the jar artifact should be generated, and the `finalName` parameter should be set to the desired name of the jar artifact. This will have the same effect as setting the `finalName` parameter alone.
