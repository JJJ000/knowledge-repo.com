---
title: Can pip be used to install a package from a private github repository?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Yes, it is possible to use pip to install a package from a private GitHub repository in Python.
---

**Contents**

[TOC]

## Yes

Yes, it is possible to use pip to install a package from a private GitHub repository in Python.

## Setup

In order to use pip to install a package from a private GitHub repository, you must first set up a personal access token. This token can be generated in the settings of your GitHub account. Once you have generated the token, you can use it as a username when installing the package with pip.

## Installation

To install the package, you can use the following command:

```
pip install git+https://<token>@github.com/<user>/<repo>.git
```

Where `<token>` is your personal access token, `<user>` is the GitHub user who owns the repository, and `<repo>` is the name of the repository.

## Notes

It is important to note that if you are using a private repository, you must use the `git+https` protocol. You cannot use the `git+ssh` protocol. Additionally, if you are using a private repository, you must include your personal access token in the URL.
