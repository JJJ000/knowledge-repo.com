---
title: What is the benefit of setting core.autocrlf to true in git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Core.autocrlf=true ensures that line endings in files are consistent across operating systems.
---

**Contents**

[TOC]

### Benefits

1. Improved Cross-Platform Compatibility: Core.autocrlf=true ensures that line endings are consistent across different operating systems. This prevents issues with code not working properly when it is transferred between different platforms.

2. Reduced Conflict Resolution: Core.autocrlf=true reduces the number of conflicts that arise when merging branches in a Git repository. Without this setting, different line endings can cause conflicts when merging branches, as Git interprets them as changes to the code.

### Drawbacks

1. Potential Issues with Binary Files: Core.autocrlf=true can cause issues with binary files, as it will attempt to change their line endings. This can cause the files to become corrupted and unusable.

2. Unnecessary Changes: Core.autocrlf=true can cause unnecessary changes to files, as it will attempt to change all line endings even if they are already consistent across platforms. This can lead to unnecessary commits and extra work.
