---
title: When attempting to download the Java jdk on linux using wget, the license page is displayed instead
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: You may need to use the `--no-check-certificate` flag when using wget to download the Java JDK.
---

**Contents**

[TOC]

### Overview

Java JDK is a software development kit used to develop Java applications and applets. It contains the Java Runtime Environment (JRE), the Java compiler and other necessary components. Downloading Java JDK on Linux via wget can be done from the official Oracle website. However, if you are presented with a license page instead of the download page, this means that you need to accept Oracle’s license agreement before you can download the JDK. 

### Accepting the License Agreement

In order to accept Oracle’s license agreement and download the JDK, you need to add an additional argument to the wget command. The argument you need to add is “--no-check-certificate” which will bypass the license agreement page and allow you to download the JDK.

### Example

For example, if you are downloading the Java JDK 8u241 from Oracle’s website, the command you would use is: 

`wget --no-check-certificate --no-cookies --header "Cookie: oraclelicense=accept-securebackup-cookie" http://download.oracle.com/otn-pub/java/jdk/8u241-b07/1f5b5a70bf22433b84d0e960903adac8/jdk-8u241-linux-x64.tar.gz`

### Conclusion

In conclusion, downloading Java JDK on Linux via wget can be done by adding the “--no-check-certificate” argument to the wget command. This will bypass the license agreement page and allow you to download the JDK.
