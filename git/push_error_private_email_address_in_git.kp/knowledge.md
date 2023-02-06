---
title: Your push would make a private email address public
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You should not push commits that contain private information, such as email addresses.
---

**Contents**

[TOC]

# Overview
This error is encountered when attempting to push a commit to a remote repository and the commit contains a private email address. This error is a safety measure to protect the privacy of the user whose email address is included in the commit.

# Causes
The error is triggered when the commit contains an email address that is not publicly available. This can occur when a user has not configured their Git settings to use their public email address, or when a user has included a private email address in the commit.

# Solutions
In order to resolve this error, the user should ensure that their Git settings are configured to use their public email address. Additionally, any private email addresses that were included in the commit should be removed before attempting to push the commit again.
