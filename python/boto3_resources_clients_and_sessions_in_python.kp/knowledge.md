---
title: What is the distinction between resource, client, and session in boto3?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: A boto3 resource represents an object-oriented interface to an AWS service, a boto3 client provides low-level direct access to AWS APIs, and a boto3 session stores configuration state and parameters to be used in the other two components.
---

**Contents**

[TOC]

### Resource
A resource is an object-oriented interface to Amazon Web Services (AWS). It allows you to access and manage AWS services in a programmatic way.

### Client
A client is a low-level interface to a service. It provides a direct access to the underlying API operations. It is generally used for more granular control over the service.

### Session
A session is a collection of configuration data that is used to interact with services. It is used to store authentication credentials, region information, and other configurations. It is used to create clients and resources.
