---
title: An error has occurred headers cannot be modified after they have been sent to the client
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Once a response has been sent to the client, the headers cannot be modified.
---

**Contents**

[TOC]

# Overview

When attempting to send multiple headers in a response, an error may be thrown stating "Can't set headers after they are sent to the client". This error is caused by attempting to send multiple headers in the same response.

# Causes

This error is caused by attempting to send multiple headers in the same response. This may be done inadvertently, for example when a response is sent multiple times in the same code block. It can also be caused by attempting to send a header after the response has already been sent.

# Solutions

To avoid this error, ensure that only one response is sent per code block. Additionally, any headers must be sent before the response is sent. If multiple headers are necessary, they must be sent in the same response.
