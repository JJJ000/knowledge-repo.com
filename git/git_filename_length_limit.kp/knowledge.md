---
title: Git for windows is unable to handle filenames that are too long
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: Git for Windows has a maximum filename length of 260 characters.
---

**Contents**

[TOC]

1. Maximum File Length

Git for Windows has a maximum file length of 255 characters. This includes the directory path, filename, and any extension.

2. Impact of Long Filenames

If a filename is longer than 255 characters, Git for Windows will not be able to track the file. This means that changes to the file will not be recorded in the repository and the file will not be included in commits.

3. Workarounds

If a filename is longer than 255 characters, it can be shortened or renamed. Additionally, the directory path can be shortened by moving the file to a shorter directory.

4. Alternative Solutions

Git for Windows is not the only version control system available. Other systems, such as Mercurial, may have different file length limits or may not have a limit at all. It may be worth exploring these other systems if the 255 character limit is too restrictive.
