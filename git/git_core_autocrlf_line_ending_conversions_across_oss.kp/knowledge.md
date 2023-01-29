---
title: What are the differences in line ending conversions when using git core.autocrlf across different operating systems?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Git core.autocrlf automatically converts line endings to the platform-specific style when pushing and pulling between different operating systems.
---

**Contents**

[TOC]

`**` What is core.autocrlf?**

Core.autocrlf is a setting in Git that determines how line endings are handled when files are committed and checked out. It is set to true by default, which means that Git will convert all line endings to the native style of the operating system it is running on. This ensures that files with different line endings will be consistent when they are shared between different operating systems.

`**` How Does Core.autocrlf Work?**

When core.autocrlf is set to true, Git will automatically convert line endings when files are committed and checked out. When a file is committed, Git will convert all line endings to the native style of the operating system it is running on. When a file is checked out, Git will convert all line endings to the native style of the operating system it is running on.

`**` What Are the Benefits of Using Core.autocrlf?**

Using core.autocrlf ensures that files with different line endings will be consistent when they are shared between different operating systems. This makes it easier for developers to collaborate across different platforms. It also helps to avoid conflicts when merging changes from different operating systems.

`**` How Can Core.autocrlf Be Configured?**

Core.autocrlf can be configured in the Git configuration file, which is located in the .git directory. The setting can be set to true, false, or input. Setting it to true will cause Git to convert all line endings to the native style of the operating system it is running on. Setting it to false will cause Git to not convert any line endings, and setting it to input will cause Git to only convert line endings when committing files.
