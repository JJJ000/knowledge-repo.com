---
title: Retrieving the ip address of the current computer with java
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: In Java, the InetAddress class can be used to get the IP address of the current machine.
---

**Contents**

[TOC]

### Using InetAddress

The InetAddress class can be used to get the IP address of the current machine. The following code snippet can be used to get the IP address of the current machine:

```java
InetAddress ip = InetAddress.getLocalHost();
String ipAddress = ip.getHostAddress();
System.out.println("Current IP address : " + ipAddress);
```

### Using NetworkInterface

The NetworkInterface class can be used to get the IP address of the current machine. The following code snippet can be used to get the IP address of the current machine:

```java
Enumeration<NetworkInterface> interfaces = NetworkInterface.getNetworkInterfaces();
while (interfaces.hasMoreElements()) {
    NetworkInterface iface = interfaces.nextElement();
    // filters out 127.0.0.1 and inactive interfaces
    if (iface.isLoopback() || !iface.isUp())
        continue;

    Enumeration<InetAddress> addresses = iface.getInetAddresses();
    while(addresses.hasMoreElements()) {
        InetAddress addr = addresses.nextElement();
        String ipAddress = addr.getHostAddress();
        System.out.println("Current IP address : " + ipAddress);
    }
}
```

### Using Socket

The Socket class can be used to get the IP address of the current machine. The following code snippet can be used to get the IP address of the current machine:

```java
Socket socket = new Socket("google.com", 80);
String ipAddress = socket.getLocalAddress().getHostAddress();
System.out.println("Current IP address : " + ipAddress);
```

### Using DatagramSocket

The DatagramSocket class can be used to get the IP address of the current machine. The following code snippet can be used to get the IP address of the current machine:

```java
DatagramSocket socket = new DatagramSocket();
String ipAddress = socket.getLocalAddress().getHostAddress();
System.out.println("Current IP address : " + ipAddress);
```
