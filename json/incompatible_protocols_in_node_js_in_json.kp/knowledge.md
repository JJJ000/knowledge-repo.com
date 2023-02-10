---
title: Error in node js the protocol "https" is not supported. it should be "http"
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: The URL protocol must be `http` instead of `https` for JSON requests.
---

**Contents**

[TOC]

# Section 1: Overview

Node.js is a JavaScript runtime environment used to execute code on the server side. It is an open-source, cross-platform runtime environment for developing server-side and networking applications. Node.js applications are written in JavaScript and can be run within the Node.js runtime on various platforms including Linux, macOS, Microsoft Windows, and more.

# Section 2: Error

When attempting to parse a JSON object in Node.js, the following error may be encountered: "Protocol "https:" not supported. Expected "http:"". This error occurs when the JSON object is being parsed with a protocol other than "http:".

# Section 3: Cause

The cause of this error is that the Node.js runtime does not support the "https:" protocol when parsing JSON objects. The "https:" protocol is a secure version of the "http:" protocol and is used when transmitting sensitive data over the internet.

# Section 4: Solution

The solution is to use the "http:" protocol when parsing JSON objects in Node.js. This can be done by explicitly setting the protocol in the URL or by using the "http:" protocol when constructing the JSON object.
