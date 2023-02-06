---
title: What are the major distinctions between soap and restful web services in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: SOAP is a protocol, while REST is an architectural style.
---

**Contents**

[TOC]

**1. Message Format**

SOAP: SOAP uses XML as a message format. 

RESTful: RESTful web services use either XML or JSON as a message format. 

**2. Statefulness**

SOAP: SOAP is a stateful protocol, which means that the server stores information about the client session on the server side. 

RESTful: RESTful web services are stateless, meaning that the server does not store any state information about the client session on the server side. 

**3. Protocols**

SOAP: SOAP uses HTTP as a transport protocol and is based on a request-response model. 

RESTful: RESTful web services use HTTP as a transport protocol and can be based on a request-response model or a publish-subscribe model. 

**4. Security**

SOAP: SOAP supports WS-Security, which provides message-level security. 

RESTful: RESTful web services support HTTPS, which provides transport-level security.
