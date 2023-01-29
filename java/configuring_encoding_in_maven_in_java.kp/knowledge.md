---
title: What is the process for setting up the encoding in maven?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: In Maven, encoding can be configured by setting the <project.build.sourceEncoding> property in the pom.xml file.
---

**Contents**

[TOC]

1. Setting the Source File Encoding 

To configure the source file encoding, you can add the following configuration to your `pom.xml`:

```
<project>
  ...
  <build>
    <plugins>
      <plugin>
        <groupId>org.apache.maven.plugins</groupId>
        <artifactId>maven-compiler-plugin</artifactId>
        <version>3.8.1</version>
        <configuration>
          <source>1.8</source>
          <target>1.8</target>
          <encoding>UTF-8</encoding>
        </configuration>
      </plugin>
    </plugins>
  </build>
  ...
</project>
```

2. Setting the File Encoding for Resources

You can also configure the file encoding for resources by adding the following configuration to your `pom.xml`:

```
<project>
  ...
  <build>
    <plugins>
      <plugin>
        <groupId>org.apache.maven.plugins</groupId>
        <artifactId>maven-resources-plugin</artifactId>
        <version>3.1.0</version>
        <configuration>
          <encoding>UTF-8</encoding>
        </configuration>
      </plugin>
    </plugins>
  </build>
  ...
</project>
```

3. Setting the Output File Encoding

You can also configure the output file encoding by adding the following configuration to your `pom.xml`:

```
<project>
  ...
  <build>
    <plugins>
      <plugin>
        <groupId>org.apache.maven.plugins</groupId>
        <artifactId>maven-surefire-plugin</artifactId>
        <version>2.22.1</version>
        <configuration>
          <encoding>UTF-8</encoding>
        </configuration>
      </plugin>
    </plugins>
  </build>
  ...
</project>
```

4. Setting the Default File Encoding

You can also set the default file encoding for the JVM by adding the following configuration to your `pom.xml`:

```
<project>
  ...
  <build>
    <plugins>
      <plugin>
        <groupId>org.apache.maven.plugins</groupId>
        <artifactId>maven-surefire-plugin</artifactId>
        <version>2.22.1</version>
        <configuration>
          <argLine>-Dfile.encoding=UTF-8</argLine>
        </configuration>
      </plugin>
    </plugins>
  </build>
  ...
</project>
```
