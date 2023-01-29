---
title: What is the method for determining if an Android device has an internet connection? using inetaddress will not cause a timeout
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Yes, InetAddress does not time out in Java, so it can be used to check for internet access on Android.
---

**Contents**

[TOC]

1. Using InetAddress

InetAddress is a Java class that can be used to check whether a particular host is reachable or not. It can be used to check whether a particular website is reachable or not. The InetAddress class has a method called isReachable() which takes a timeout in milliseconds as an argument. If the host is reachable within the given timeout, it will return true, otherwise it will return false.

2. Checking Internet Access

To check whether the device has internet access, you can use the isReachable() method of the InetAddress class to check whether a particular website is reachable or not. If the website is reachable within the given timeout, then the device has internet access.

3. InetAddress Never Times Out

InetAddress never times out in Java. The isReachable() method of the InetAddress class will always return true or false depending on whether the host is reachable or not. It will never throw an exception or timeout.

4. Conclusion

InetAddress is a Java class that can be used to check whether a particular host is reachable or not. To check whether the device has internet access, you can use the isReachable() method of the InetAddress class to check whether a particular website is reachable or not. InetAddress never times out in Java.
