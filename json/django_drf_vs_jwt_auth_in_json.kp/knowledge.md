---
title: Comparing django rest framework token-based authentication to JSON web token authentication
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-16 00:00:00
updated_at: 2023-02-16 00:00:00
tldr: DRF Token based Authentication is a built-in authentication system for Django, while JSON Web Token is an external authentication system for any application.
---

**Contents**

[TOC]

# Django Rest Framework Token Based Authentication

Django Rest Framework (DRF) token based authentication is a powerful authentication method that utilizes tokens instead of traditional username/password authentication. This authentication type is useful for web applications that require a high degree of security and scalability.

DRF token based authentication uses a token-based authentication system for user authentication. The token is generated when the user logs in, and is used to authenticate the user for subsequent requests. The token is stored in a database and is associated with the user's account.

The token is sent as part of the request header and is used to authenticate the user for each request. The token is also used to verify that the user is authorized to access the requested resource.

# JSON Web Token

JSON Web Token (JWT) is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object. This information can be verified and trusted because it is digitally signed. JWTs can be signed using a secret (with the HMAC algorithm) or a public/private key pair using RSA or ECDSA.

JWT is used to securely transmit information between two parties. It is commonly used in authentication and authorization scenarios, as well as for securely exchanging data between parties. JWT is also used for securely transmitting information between client and server, such as an API token.

JWT is used to securely transmit data between two parties. It is a secure way of exchanging data between two parties, as the data is digitally signed and encrypted. JWT is also used for securely exchanging data between client and server, such as an API token.
