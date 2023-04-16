---
title: What steps do I need to take to enable jmx on my jvm so I can use jconsole?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Add the following JVM options to enable JMX -Dcom.sun.management.jmxremote and -Dcom.sun.management.jmxremote.port=<port\_number>.
---

**Contents**

[TOC]

## Step 1: Create the JVM Arguments 
To enable JMX on the JVM, you must add the following JVM arguments to the JVM startup command: 

`-Dcom.sun.management.jmxremote` 
`-Dcom.sun.management.jmxremote.port=<port>` 
`-Dcom.sun.management.jmxremote.authenticate=false` 
`-Dcom.sun.management.jmxremote.ssl=false` 

Replace `<port>` with the port number you want to use for JMX. 

## Step 2: Start the JVM 
Start the JVM with the JVM arguments you created in Step 1. 

## Step 3: Connect to the JVM with jconsole 
Once the JVM is running, you can connect to it with jconsole. To do this, open a terminal and type the following command: 

`jconsole <host>:<port>` 

Replace `<host>` with the hostname of the machine running the JVM and `<port>` with the port number you used in Step 1. 

## Step 4: Enable JMX on the JVM 
When you connect to the JVM with jconsole, you will be prompted to enable JMX on the JVM. Click the “Enable” button to enable JMX on the JVM.
