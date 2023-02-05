---
title: The '_xsrf' argument is missing from the post when attempting to save a jupyter notebook
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The `\_xsrf` argument is required for the post request in order to save the Jupyter Notebook.
---

**Contents**

[TOC]

1. Overview 

Jupyter Notebook is a web-based interactive computing environment that allows users to create and share documents containing live code, equations, visualizations, and narrative text. It is a popular tool for data scientists, researchers, and students. However, occasionally users may encounter an issue where the Jupyter Notebook is not saving their changes. One possible cause of this issue is the '_xsrf' argument missing from the post in Python. In this article, we will discuss the causes of this issue and how to fix it. 

2. What is the '_xsrf' Argument?

The '_xsrf' argument is a security feature that is used to protect against Cross-Site Request Forgery (CSRF) attacks. It is sent with each request to the server, and the server checks it against a known value to make sure that the request is legitimate. If the value does not match, then the request is rejected. 

3. Causes of the Issue 

The '_xsrf' argument is missing from the post in Python when the web browser has disabled cookies. When the cookies are disabled, the '_xsrf' argument is not sent with the request, and the server will reject the request. 

4. How to Fix the Issue 

To fix the issue, the user must enable cookies in their web browser. To do this, they must go to the browser's settings and enable cookies. Once the cookies are enabled, the '_xsrf' argument will be sent with the request, and the Jupyter Notebook will save the changes.
