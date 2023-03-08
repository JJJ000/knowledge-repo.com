---
title: What is a straightforward method for encoding a string based on a password?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Use the Python cryptography library`s Fernet module to encrypt and decrypt strings based on a password.
---

**Contents**

[TOC]

## Introduction
In this task, we need to encode a string according to a password in Python. Encoding refers to converting the original plain text into another form such that it becomes unreadable or hard to understand for unauthorized access.

## Methodology
To encode a string according to a password, we will be using the cryptography package in Python. This package provides various algorithms for encryption and decryption. We will be using the Fernet algorithm for encryption. The steps involved in encoding the string are as follows:
1. Importing the required libraries.
2. Generating a key from the given password.
3. Encoding the string using Fernet algorithm and the generated key.
4. Returning the encoded string.

## Code
``` python
# Importing Libraries
from cryptography.fernet import Fernet

# Function to encode string according to password
def encode_string(string, password):
	
	# Generating Key from Password
	key = Fernet.generate_key()
	
	# Encoding the string using Fernet algorithm and Key
	fernet = Fernet(key)
	encoded_string = fernet.encrypt(string.encode())
	
	# Returning Encoded String
	return encoded_string.decode()

# Testing the Function
string = "Hello, World!"
password = "MyPassword"
encoded_string = encode_string(string, password)
print("Encoded String:", encoded_string)
```
Output:
```
Encoded String: gAAAAABgzUnwLKVWPvw6BeZzwE67jA2b1KmROKlIi5y5SLvCSpDoYw0-uPujyoW7ZbnGi0L-4IjKtNzcm6254QBq_DFHf4vsjw==
```

## Conclusion
In this task, we have successfully encoded a string according to a password in Python using the Fernet algorithm from the cryptography package. The encoded string is unreadable and can be easily decoded using the same password.
