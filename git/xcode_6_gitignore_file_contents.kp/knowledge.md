---
title: What should be included in the xcode 6 gitignore file?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Xcode 6 gitignore file should include entries for build products, private settings, and temporary files.
---

**Contents**

[TOC]

1. Source Code:
    - *.swift
    - *.h
    - *.m

2. Build Products:
    - *.xcworkspace
    - *.xcuserstate
    - *.xcodeproj
    - DerivedData

3. IDE Settings:
    - *.mode1v3
    - *.pbxuser
    - *.perspectivev3

4. Other:
    - *.DS_Store
    - *.git
    - *.gitignore
