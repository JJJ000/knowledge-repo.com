---
title: Could you explain the dissimilarity between aws boto and boto3?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Boto is the older version while boto3 is the newer, redesigned version of the AWS SDK for Python.
---

**Contents**

[TOC]

# Introduction
AWS (Amazon Web Services) provides both `boto` and `boto3` for interacting and managing their cloud services through various programming interfaces. These libraries are popular for Python programming, but they differ in various dimensions.

# Version
`boto` is the first version of the Python library that added support for the AWS services, while `boto3` is the latest version that has been designed to fix issues observed in `boto` and bring new features.

# Syntax
`boto` and `boto3` have different syntaxes when it comes to accessing the AWS services. `boto` uses a procedural style syntax that makes it easy to learn and use for beginners, while `boto3` uses an object-oriented interface, which is a little bit harder to learn than `boto`. However, once you learn `boto3`, it will make your work more comprehensive, reusable, and easier to maintain.

# Future Support
Despite the `boto` library having been widely used in the past, it is slowly falling out of favor as `boto3` gains prominence, mainly because `boto3` has much better community support and more robust features compared to `boto`. Thus, if you plan to work on AWS going forward, we recommend using `boto3`, which has better scope and support for the current and future AWS services.
