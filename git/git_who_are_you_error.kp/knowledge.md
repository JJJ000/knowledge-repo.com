---
title: What is your identity? git is asking for your information
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Git does not understand this command, as it is not a valid Git command.
---

**Contents**

[TOC]

### Introduction

Git is a version control system that is used to track changes in computer files and directories. It is used to store and track changes to files, and also to share and collaborate with other users.

### Error Message

When attempting to use Git, you may receive the following error message: "please tell me who you are". This is an authentication error and indicates that Git does not recognize the user.

### Resolution

In order to resolve this error, you must configure Git with your name and email address. This can be done by running the following command:

`git config --global user.name "Your Name"`

`git config --global user.email "your@email.com"`

Once this is done, you should be able to use Git without any further issues.

### Conclusion

In conclusion, the "please tell me who you are" error message is an authentication error. It can be resolved by configuring Git with your name and email address. Once this is done, you should be able to use Git without any further issues.
