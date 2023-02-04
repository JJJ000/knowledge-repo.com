---
title: What is the process for deciphering a jwt token in JavaScript without using a library?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use an algorithm such as Base64 to decode the jwt token.
---

**Contents**

[TOC]

# Section 1: Decoding the Header

The header of a JWT token is a JSON object that is Base64Url encoded. To decode the header, we must first Base64Url decode the header, then parse the resulting string as a JSON object.

# Section 2: Decoding the Payload

Similar to the header, the payload of a JWT token is a JSON object that is Base64Url encoded. To decode the payload, we must first Base64Url decode the payload, then parse the resulting string as a JSON object.

# Section 3: Verifying the Signature

The signature of a JWT token is a HMAC-SHA256 hash of the encoded header and payload. To verify the signature, we must generate a HMAC-SHA256 hash of the encoded header and payload using the same secret key used to generate the signature, then compare the generated hash with the signature provided.

# Section 4: Putting it All Together

To decode a JWT token without using a library, we must first Base64Url decode the header and payload, then parse the resulting strings as JSON objects. We must then generate a HMAC-SHA256 hash of the encoded header and payload using the same secret key used to generate the signature, then compare the generated hash with the signature provided. If the hashes match, the JWT token is valid and can be used.
