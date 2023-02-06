---
title: Git encountered 7 files that should have been symbolic links, but were not
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: This indicates that the expected Git LFS pointer files were not found in the repository.
---

**Contents**

[TOC]

**Cause**

This error occurs when Git finds files that it expects to be pointers, but they are not. A pointer is a type of object in Git which is used to reference another object, such as a commit or a tree. When Git encounters a file that it expects to be a pointer, but isn't, it will return this error.

**Examples**

This error can occur for a variety of reasons, such as when a file is corrupted or when a file is not properly formatted as a pointer. For example, if a file is missing the "object" field, or if the "type" field is incorrect, then Git will return this error.

**Troubleshooting**

The first step in troubleshooting this error is to identify the files that are causing the issue. This can be done by running the command `git fsck --full` which will list out all of the files that Git is expecting to be pointers, but aren't.

Once the files have been identified, the next step is to examine the contents of the files and determine why Git is expecting them to be pointers. This can be done by manually inspecting the contents of the file, or by using a tool such as `git cat-file` to examine the contents of the file.

**Resolution**

Once the cause of the issue has been identified, the next step is to fix the problem. This can be done by manually editing the file to ensure that it is properly formatted as a pointer, or by using a tool such as `git hash-object` to create a new pointer object. Once the file has been fixed, it should be added back to the repository using the `git add` command.
