---
title: Calculating a file's md5 hash in java
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The MessageDigest class can be used to calculate a file`s MD5 checksum in Java.
---

**Contents**

[TOC]

### Using the Java Cryptography Architecture
1. Import the necessary packages: `import java.security.*;`
2. Create a `MessageDigest` instance: `MessageDigest md = MessageDigest.getInstance("MD5");`
3. Read the file and update the `MessageDigest` instance with its contents: `FileInputStream fis = new FileInputStream(file); byte[] dataBytes = new byte[1024]; int nread = 0; while ((nread = fis.read(dataBytes)) != -1) { md.update(dataBytes, 0, nread); };`
4. Generate the checksum: `byte[] mdbytes = md.digest();`

### Using Apache Commons Codec
1. Import the necessary packages: `import org.apache.commons.codec.digest.DigestUtils;`
2. Read the file and generate the checksum: `String md5 = DigestUtils.md5Hex(new FileInputStream(file));`
