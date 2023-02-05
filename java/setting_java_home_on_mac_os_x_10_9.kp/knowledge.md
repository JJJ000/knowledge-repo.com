---
title: What is the process for establishing the java_home environment variable on mac os x 10.9?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Set the JAVA\_HOME environment variable to the path of the JDK installation directory.
---

**Contents**

[TOC]

1. **Check Installed Java Version:**

Before setting the JAVA_HOME environment variable, you should check which version of Java is installed on your system. You can check the installed version of Java by running the following command in the terminal:

`/usr/libexec/java_home`

2. **Set JAVA_HOME Environment Variable:**

Once you have determined the installed version of Java, you can set the JAVA_HOME environment variable by running the following command in the terminal:

`export JAVA_HOME=`/usr/libexec/java_home`

3. **Verify JAVA_HOME Environment Variable:**

You can verify that the JAVA_HOME environment variable has been set correctly by running the following command in the terminal:

`echo $JAVA_HOME`

4. **Add JAVA_HOME to PATH Variable:**

If you want to add JAVA_HOME to the PATH variable, you can do so by running the following command in the terminal:

`export PATH=$JAVA_HOME/bin:$PATH`
