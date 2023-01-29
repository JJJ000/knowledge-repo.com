---
title: Change keystore passwords
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: To change passwords in Java, use the KeyStore.load() method with the new password.
---

**Contents**

[TOC]

### Overview

Changing passwords in Java involves a few steps. First, the user must create a new keystore with the desired password. Then, the user must update the application configuration to use the new keystore. Finally, the user must update the application code to use the new password.

### Create a New Keystore

The first step in changing the password in Java is to create a new keystore with the desired password. This can be done using the `keytool` command line utility. The command to create a new keystore is `keytool -genkey -alias <alias> -keystore <keystore> -storepass <password>` where `<alias>` is the name of the keystore, `<keystore>` is the path to the keystore, and `<password>` is the desired password.

### Update the Application Configuration

The next step is to update the application configuration to use the new keystore. This can be done by changing the `javax.net.ssl.keyStore` and `javax.net.ssl.keyStorePassword` system properties to point to the new keystore and password.

### Update the Application Code

Finally, the application code must be updated to use the new password. This can be done by calling the `setKeyStorePassword` method on the `SSLContext` object. This method takes the new password as an argument.
