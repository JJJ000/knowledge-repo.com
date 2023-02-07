---
title: Websockets client API http headers
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The Websockets client API in Javascript does not have any HTTP headers associated with it.
---

**Contents**

[TOC]

#### Access-Control-Allow-Origin
This header is used to specify which domains have access to a resource. It is used to prevent cross-site scripting (XSS) attacks.

#### Sec-WebSocket-Protocol
This header specifies the sub-protocols that the client is willing to speak. It is used to determine which protocol is used for communication between the client and server.

#### Sec-WebSocket-Version
This header specifies the version of the WebSocket protocol that the client is using. It is used to ensure that the client and server are using the same version of the protocol.

#### Sec-WebSocket-Extensions
This header specifies the extensions that the client supports. It is used to enable additional features such as compression, authentication, and encryption.
