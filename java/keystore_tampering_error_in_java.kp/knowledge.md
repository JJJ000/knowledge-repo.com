---
title: The keytool encountered an error indicating that either the keystore had been compromised or the password was incorrect
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The keystore could not be accessed due to an incorrect password or tampering.
---

**Contents**

[TOC]

# Answer

## Symptoms
When attempting to access a Java keystore, the following error message may appear:

```
keytool error: java.io.IOException: Keystore was tampered with, or password was incorrect
```

## Cause
This error occurs when the keystore file is corrupted or the password used to access the keystore is incorrect.

## Resolution

1. Check that the keystore file is not corrupted.
2. Verify that the correct password is being used to access the keystore.
3. If the keystore file is corrupted, try restoring it from a backup.
