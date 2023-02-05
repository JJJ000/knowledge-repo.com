---
title: What is the command to disable the Maven javadoc plugin from the command line?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Run the command `mvn javadocjavadoc -Dskip` to disable the Maven Javadoc plugin from the command line.
---

**Contents**

[TOC]

1. Unbind the Plugin from the Project
-------------------------------------
Open the `pom.xml` file of the project and find the `<plugin>` element corresponding to the Maven Javadoc plugin. Then, add the following attribute to the element:

```
<plugin>
    ...
    <configuration>
        <skip>true</skip>
    </configuration>
    ...
</plugin>
```

2. Execute the Build
--------------------
Execute the build with the `-Dskip` flag, like so:

```
mvn clean install -Dskip
```

3. Disable the Plugin Globally
------------------------------
Open the `settings.xml` file in the `.m2` directory and find the `<plugin>` element corresponding to the Maven Javadoc plugin. Then, add the following attribute to the element:

```
<plugin>
    ...
    <configuration>
        <skip>true</skip>
    </configuration>
    ...
</plugin>
```

4. Execute the Build
--------------------
Execute the build with the `-Dskip` flag, like so:

```
mvn clean install -Dskip
```
