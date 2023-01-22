---
title: How to store binary data as a JSON-encoded string instead of base64?
authors:
- cool_wizard
tags:
- base64
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-01-22 00:00:00
updated_at: 2023-01-22 00:00:00
tldr: Base64 is the most common way to encode binary data in JSON strings, but other methods such as Hex encoding may provide better performance.
---

**Contents**

[TOC]

### What is Base64?
Base64 is a binary-to-text encoding scheme that encodes binary data into a string of ASCII characters. It is used to transfer data over the internet and is commonly used to encode binary data such as images, audio, and video.

### Limitations of Base64
Base64 has several limitations, including: 

1) It is not as efficient as other encoding methods. Base64 encoding increases the size of the data by 33%, making it less efficient than other methods such as gzip compression. 

2) It is not secure. Base64 is not an encryption method, so it does not provide any security to the data. It is vulnerable to brute-force attacks, where an attacker can easily guess the encoded data.

3) It is not supported by all browsers. Some browsers may not support Base64 encoding, making it difficult to use in some cases.

### Alternatives to Base64
There are several alternatives to Base64 that can be used to encode binary data in JSON strings. These alternatives are more efficient, secure, and supported by more browsers.

1) JSON Web Tokens (JWT): JWT is an open standard that defines a compact and self-contained way for securely transmitting information between parties as a JSON object. It is more secure than Base64, as it uses a digital signature to verify the integrity of the data.

2) Asymmetric encryption: Asymmetric encryption is a type of encryption that uses two different keys (a public key and a private key) to encrypt and decrypt data. It is more secure than Base64, as it is not vulnerable to brute-force attacks.

3) Base64url: Base64url is an alternative to Base64 that is more efficient and supported by more browsers. It is not as secure as JWT or asymmetric encryption, but it is still more secure than Base64.

### Conclusion
Base64 is a popular method for encoding binary data in JSON strings, but it has several limitations. Alternatives such as JSON Web Tokens, asymmetric encryption, and Base64url are more efficient, secure, and supported by more browsers.
