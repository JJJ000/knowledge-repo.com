---
title: Concealing a password in a Python script (only a weak form of obfuscation)
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: It is not secure to hide a password in a Python script using insecure obfuscation methods.
---

**Contents**

[TOC]

## Why hiding passwords in a Python script is a bad idea?

Before discussing the techniques for password obfuscation in a Python script, it is important to understand the reasons why it is not a good practice. The primary reasons are:

- Easily discoverable: Python scripts are usually stored as plain text files that can be accessed and read by anyone who has access to the system. As a result, any password stored in the script can be easily discovered.

- No encryption: Passwords stored in plain text format are not encrypted, making them vulnerable to attacks such as eavesdropping, interception, or theft.

- Limited scope of protection: If you have to protect your password present in the script, then you need to take extra precautions. Obfuscation can provide limited protection, but it is not a substitute for proper security measures such as encryption and access control.

## Techniques for insecure obfuscation of password

Despite the security limitations of obfuscation techniques, it is still possible to protect the passwords present in your Python scripts using the following techniques:

### Technique 1: Encoding passwords using base64

One of the simplest techniques to obfuscate passwords in a Python script is to encode them using base64. The following code demonstrates how to encode a password using base64 in Python:

```python
import base64

password = b'password'
enc_password = base64.b64encode(password)
print(enc_password)
```

The resulting output of the code will look something like this: `b'cGFzc3dvcmQ='`

You can use the encoded password in your Python script and decode it as needed. However, note that base64 encoding is a weak form of obfuscation and can be easily decoded.

### Technique 2: Storing passwords in a separate file

Another technique to obfuscate passwords in a Python script is to store them in a separate file. You can then read the password from the file and use it in your script as needed. This approach helps to keep the password separate from the code, making it less visible to an attacker.

```python

with open("password.txt", "r") as file:
    password = file.read()

print(password)

```

Again, note that storing passwords in a separate file is not a secure practice and provides limited protection.

### Technique 3: Using environment variables

Another technique to obfuscate passwords in a Python script is to use environment variables. Environment variables are variables that are set in the system environment and can be accessed by applications running on the system.

```python

import os

password = os.environ.get('PASSWORD')
print(password)

```

You can set the environment variable in the system where the Python script will run, and the script can retrieve it using the `os.environ.get()` method. However, note that environment variables can be easily accessed and modified by users who have access to the system. 

## Conclusion

Hiding passwords in a Python script using insecure obfuscation techniques such as base64 encoding, storing in a separate file, or environment variables, can provide limited protection, but it is not a substitute for proper security measures such as encryption and access control. It is always recommended to use a secure approach such as using external password management services or using a secure key management system to store and manage your passwords.
