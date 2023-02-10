---
title: Is it standard practice to update multiple resources with a single request using rest, or should it be avoided?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Updating multiple resources with one request is not a standard practice in JSON.
---

**Contents**

[TOC]

# Introduction

Updating multiple resources with one request is a common operation in web applications. In JSON, it is possible to update multiple resources in one request, but whether or not it should be done depends on the application and its use case.

# Advantages

One of the main advantages of updating multiple resources in one request is that it can be more efficient than making multiple requests. This can reduce the amount of time and resources needed to complete the operation. Additionally, it can make the process more convenient for the user, as they don't have to make multiple requests.

# Disadvantages

The main disadvantage of updating multiple resources in one request is that it can be more difficult to debug and maintain. This can be especially true if the request contains complex data structures or if it is sent to a web service with limited logging capabilities. Additionally, if the request fails, it can be difficult to determine which resource failed, as all of the resources would need to be rolled back.

# Conclusion

Whether or not it is standard or to be avoided in JSON depends on the application and its use case. Updating multiple resources in one request can be more efficient and convenient for the user, but it can also be more difficult to debug and maintain. Therefore, it is important to weigh the pros and cons before deciding whether or not to use this approach.
