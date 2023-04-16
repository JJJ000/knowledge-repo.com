---
title: Is it secure to make the firebase apikey accessible to everyone?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: No, it is not safe to expose Firebase apiKey to the public in Javascript.
---

**Contents**

[TOC]

## No

It is not safe to expose Firebase apiKey to the public in Javascript. Firebase apiKeys are used to authenticate requests to the Firebase backend, and exposing them to the public would make it possible for malicious users to gain access to the Firebase database and make unauthorized changes.

## Security Risks

Exposing Firebase apiKeys to the public can lead to a variety of security risks, including:

- Unauthorized access to the Firebase database
- Data tampering or deletion
- Unauthorized changes to the Firebase data
- Unauthorized access to Firebase functions
- Unauthorized access to Firebase storage

## Best Practices

In order to ensure the security of Firebase apiKeys, it is best to keep them private and not expose them to the public. If the apiKey must be used in a public facing application, it is recommended to use a secure method of authentication, such as OAuth 2.0. Additionally, it is important to ensure that the apiKey is stored securely, such as in an encrypted database or environment variables.
