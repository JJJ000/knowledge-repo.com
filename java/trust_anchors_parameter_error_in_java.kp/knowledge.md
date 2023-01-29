---
title: The trustanchors parameter cannot be left blank or empty
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The trustAnchors parameter must be non-empty in order for Java to establish a trust relationship with the desired server.
---

**Contents**

[TOC]

### What is the TrustAnchors Parameter?
The TrustAnchors parameter is a parameter used by the Java KeyStore class. It is used to specify which Certificate Authorities (CAs) should be trusted when verifying digital signatures. The TrustAnchors parameter is an array of TrustAnchor objects, which can be used to specify a set of trusted CAs.

### What Does it Mean for TrustAnchors to be Non-Empty?
When the TrustAnchors parameter is non-empty, it means that there is at least one trusted CA specified in the array. If the TrustAnchors parameter is empty, then no CAs are trusted and any digital signatures cannot be verified.

### What Causes the Error?
The error occurs when the TrustAnchors parameter is empty. This can happen if the array is not initialized correctly, or if the array is emptied after it has been initialized.

### How Can the Error Be Avoided?
The error can be avoided by ensuring that the TrustAnchors parameter is initialized correctly and that it is not emptied after initialization. Additionally, the array should be populated with the appropriate TrustAnchor objects before attempting to verify any digital signatures.
