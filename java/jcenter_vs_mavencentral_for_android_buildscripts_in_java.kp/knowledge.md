---
title: What is the difference between jcenter and mavencentral when used with Android buildscripts?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: jcenter is the primary repository for Android buildscripts, while mavencentral is a supplemental repository.
---

**Contents**

[TOC]

# Introduction

Android buildscript repositories are used to share and store Android libraries, plugins, and other build-related files. They are essential for developers who need to access the latest versions of libraries and plugins for their projects. The two most popular repositories for Android buildscript are jcenter and mavencentral. 

# jcenter

jcenter is a repository hosted by Bintray, a company that specializes in hosting software packages. It is the default repository for Android Studio and is the recommended repository for Android development. It contains a vast collection of open source libraries and plugins for Android, and it is updated frequently. It is also easy to use, as it has a web-based UI that allows developers to search for libraries and plugins.

# mavencentral

MavenCentral is a repository hosted by the Apache Software Foundation. It contains a wide variety of open source libraries and plugins for Android, and it is updated regularly. It is also easy to use, as it has a command-line interface that allows developers to search for libraries and plugins. However, it is not the default repository for Android Studio, so developers must manually add it to their projects.

# Conclusion

Both jcenter and mavencentral are popular repositories for Android buildscript. jcenter is the default repository for Android Studio and is the recommended repository for Android development. It is easy to use and contains a vast collection of open source libraries and plugins. MavenCentral is also a popular repository, but it must be manually added to a project. It is updated regularly and has a command-line interface that allows developers to search for libraries and plugins.
