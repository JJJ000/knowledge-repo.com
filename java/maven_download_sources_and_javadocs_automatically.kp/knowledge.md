---
title: Maven – always obtain source code and javadocs
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: No, Maven does not always download sources and javadocs; this is configurable in the project`s pom.xml.
---

**Contents**

[TOC]

### Yes
Maven is configured by default to always download sources and javadocs for any dependency that it downloads. This behavior is enabled by setting the `downloadSources` and `downloadJavadocs` properties to `true` in the `settings.xml` file:

```xml
<settings>
  <profiles>
    <profile>
      <id>default</id>
      <activation>
        <activeByDefault>true</activeByDefault>
      </activation>
      <properties>
        <downloadSources>true</downloadSources>
        <downloadJavadocs>true</downloadJavadocs>
      </properties>
    </profile>
  </profiles>
</settings>
```

### No
It is possible to disable the default behavior of downloading sources and javadocs for all dependencies. This can be done by setting the `downloadSources` and `downloadJavadocs` properties to `false` in the `settings.xml` file:

```xml
<settings>
  <profiles>
    <profile>
      <id>default</id>
      <activation>
        <activeByDefault>true</activeByDefault>
      </activation>
      <properties>
        <downloadSources>false</downloadSources>
        <downloadJavadocs>false</downloadJavadocs>
      </properties>
    </profile>
  </profiles>
</settings>
```

It is also possible to configure Maven to download sources and javadocs for specific dependencies by adding the `<sources>` and `<javadoc>` elements to the `<dependency>` element in the `pom.xml` file.
