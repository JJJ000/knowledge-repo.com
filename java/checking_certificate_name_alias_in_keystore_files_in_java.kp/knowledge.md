---
title: What is the process for verifying the certificate name and alias in keystore files?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The certificate name and alias can be checked in keystore files in Java by using the `keytool -list` command.
---

**Contents**

[TOC]

1. Prerequisites
- Java Development Kit (JDK)
- Keystore file

2. Generating a Keystore File
- Open a Command Prompt window
- Navigate to the directory containing the keytool
- Execute the following command:

`keytool -genkey -alias <alias_name> -keystore <keystore_name> -keyalg RSA`

3. Retrieving Certificate Name and Alias
- Open a Command Prompt window
- Navigate to the directory containing the keytool
- Execute the following command:

`keytool -list -keystore <keystore_name> -v`

4. Output
- The command will output the certificate name and alias for the keystore file.
