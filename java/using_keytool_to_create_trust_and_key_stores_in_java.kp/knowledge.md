---
title: Creating key stores and trust stores using keytool
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: A Key Store is used to store private keys and certificates while a Trust Store is used to store public certificates.
---

**Contents**

[TOC]

### Key Store
A key store is a file that contains private keys, certificates, and other cryptographic information that is used to secure communication between two parties. It is used to store and manage the digital certificates and private keys for applications and servers. Key stores are used to store a user’s private keys, certificates, and other cryptographic information.

### Trust Store
A trust store is a file that contains certificates from trusted third parties. It is used to verify the identity of the server or application that is connecting to the client. The trust store contains the public keys of the trusted third parties, which are used to verify the identity of the server or application.

### Creating with keytool in Java
Keytool is a command line tool used to generate and manage keystores and certificates in Java. It can be used to create, import, export, and manage keystores and certificates. To create a key store or trust store, the keytool command is used. The command requires the following arguments:

* -genkey: Generates a key pair (public and private key) and stores it in a keystore
* -import: Imports certificates or keys into a keystore
* -export: Exports certificates or keys from a keystore
* -list: Lists the contents of a keystore

The keytool command also requires the following parameters:

* -storetype: The type of keystore, either JKS or PKCS12
* -keyalg: The algorithm used to generate the keys, such as RSA or DSA
* -keysize: The size of the key, in bits
* -alias: The name of the key or certificate in the keystore
* -keypass: The password used to protect the key in the keystore
* -storepass: The password used to protect the keystore
