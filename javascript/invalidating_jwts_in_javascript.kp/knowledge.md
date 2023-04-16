---
title: Making JSON web tokens invalid
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: JSON Web Tokens can be invalidated by calling the jwt.invalidate() method.
---

**Contents**

[TOC]

# Section 1 - Overview
A JSON Web Token (JWT) is a signed data structure that is used to securely transmit information between two parties. It is commonly used for authentication and authorization purposes, but can also be used for other purposes. JWTs are typically signed with a digital signature algorithm, such as HMAC or RSA, and are cryptographically secure.

# Section 2 - Invalidating a JWT
In order to invalidate a JWT, the signature must be invalidated. This can be done in a few different ways. The most common approach is to use a time-based invalidation mechanism. This means that the JWT will be invalidated after a certain amount of time has passed. This approach is often used in combination with a refresh token, which can be used to obtain a new JWT with a new expiration time.

# Section 3 - Implementing Time-Based Invalidation
In order to implement time-based invalidation, the JWT must include an expiration time (exp) claim. This claim should be set to the time at which the JWT should be considered invalid. When the JWT is received, the exp claim can be checked to make sure that the JWT is still valid. If the current time is greater than the exp claim, then the JWT is considered invalid and should be rejected.

# Section 4 - Other Invalidation Strategies
In addition to time-based invalidation, there are other strategies for invalidating JWTs. These include revoking tokens, which can be done by adding a revoked claim to the JWT. This claim can be checked to make sure that the JWT has not been revoked. Another approach is to use a one-time token, which is a JWT that is only valid for a single request. This approach can be used to prevent replay attacks.
