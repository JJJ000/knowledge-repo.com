---
title: Access environment variables in node.js
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Environment variables can be accessed in Node.js using the `process.env` object.
---

**Contents**

[TOC]

1. Using `process.env` 
    `process.env` is an object that holds all the environment variables as key-value pairs. To access the value of an environment variable, you can use `process.env.VAR_NAME`, where `VAR_NAME` is the name of the environment variable. 

2. Using `require('dotenv').config()`
    If you are using the `dotenv` package, you can use `require('dotenv').config()` to load environment variables from a `.env` file into `process.env`.

3. Using `require('env2')('./path/to/env/file')`
    If you are using the `env2` package, you can use `require('env2')('./path/to/env/file')` to load environment variables from a `.env` file into `process.env`.

4. Using `require('custom-env').env('./path/to/env/file')`
    If you are using the `custom-env` package, you can use `require('custom-env').env('./path/to/env/file')` to load environment variables from a `.env` file into `process.env`.
