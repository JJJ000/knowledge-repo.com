---
title: What is the process for adding a .cer certificate to a Java keystore?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the keytool command to import the .cer certificate into the Java keystore.
---

**Contents**

[TOC]

## Step 1: Extract the Private Key and Certificate

Using the OpenSSL command line utility, extract the private key and certificate from the .cer file.

```
openssl pkcs12 -in <filename>.cer -nocerts -out <filename>.key
```

## Step 2: Create a Java Keystore

Create a new Java keystore using the command line utility keytool.

```
keytool -genkey -keyalg RSA -alias <alias_name> -keystore <keystore_name>.jks
```

## Step 3: Import the Private Key and Certificate

Import the private key and certificate into the keystore.

```
keytool -importkeystore -srckeystore <filename>.key -destkeystore <keystore_name>.jks -srcstoretype PKCS12
```

## Step 4: Verify the Imported Certificate

Verify the imported certificate using the keytool command.

```
keytool -list -keystore <keystore_name>.jks
```
