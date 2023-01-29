---
title: The warning 'unable to load native-hadoop library for your platform' is displayed when hadoop is unable to find the necessary library files for the current platform
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The warning can be safely ignored if running in a non-native environment.
---

**Contents**

[TOC]

### Overview

Hadoop is an open-source software framework used for distributed storage and processing of large datasets on computer clusters built from commodity hardware. It is designed to scale up from single servers to thousands of machines, each offering local computation and storage.

When running Hadoop applications, users may encounter the "Unable to load native-hadoop library for your platform" warning. This warning indicates that the native libraries for Hadoop are not available on the system. This can cause various issues, such as slow performance or unexpected results.

### Causes

The "Unable to load native-hadoop library for your platform" warning is caused by the absence of the native libraries for Hadoop. These libraries are necessary for Hadoop to function properly.

The native libraries are platform-dependent, meaning that the libraries must be installed for the specific platform the Hadoop application is running on. If the libraries are not installed, the warning will be displayed.

### Solutions

The solution to this issue is to install the native libraries for Hadoop. The libraries can be downloaded from the Apache Hadoop website.

Once the libraries are downloaded, they must be installed in the correct location. The location of the libraries will depend on the platform the Hadoop application is running on.

### Conclusion

The "Unable to load native-hadoop library for your platform" warning is caused by the absence of the native libraries for Hadoop. To resolve this issue, the native libraries must be downloaded and installed in the correct location. Once the libraries are installed, the warning should no longer appear.
