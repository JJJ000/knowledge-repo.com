---
title: Programmatically obtain the version of an Android application
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The application version can be obtained programmatically in Android using the getPackageInfo() method of the PackageManager class.
---

**Contents**

[TOC]

1. **Using PackageInfo**

The PackageInfo class contains information about an application package that is installed on a device. It contains the version name, version code, and other information about the package.

```java
PackageInfo pInfo = getPackageManager().getPackageInfo(getPackageName(), 0);
String version = pInfo.versionName;
```

2. **Using BuildConfig**

The BuildConfig class is a generated class that contains constants that are defined in the build.gradle file.

```java
String version = BuildConfig.VERSION_NAME;
```

3. **Using Manifest**

The AndroidManifest.xml file contains information about the application such as its version name and version code.

```java
PackageManager manager = context.getPackageManager();
PackageInfo info = manager.getPackageInfo(context.getPackageName(), 0);
String version = info.versionName;
```

4. **Using PackageManager**

The PackageManager class provides a method to get information about an application package that is installed on the device.

```java
PackageManager manager = getPackageManager();
PackageInfo info = manager.getPackageInfo(getPackageName(), 0);
String version = info.versionName;
```
