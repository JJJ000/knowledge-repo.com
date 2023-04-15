---
title: Maven was unable to retrieve the artifact descriptor
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Maven failed to read the artifact descriptor because the coordinates of the artifact were incorrect.
---

**Contents**

[TOC]

### Resolution

1. Check if the artifact is available in the Maven Central Repository. If not, add the repository to the pom.xml file.
2. Ensure that the groupId, artifactId, and version are correct in the pom.xml file.
3. Check the settings.xml file and make sure that the correct mirror is configured.
4. If the issue persists, try deleting the .m2/repository folder and running the maven command again.
