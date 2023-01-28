---
title: Which files should be excluded from the .idea folder?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: All files and folders except the .name and workspace.xml files should be gitignored from the .idea folder.
---

**Contents**

[TOC]

### IntelliJ Files
* *.iml
* *.iws
* *.ipr

### Workspace Files
* workspace.xml

### Caches
* .idea/caches
* .idea/libraries

### Compiler Outputs
* .idea/compiler.xml
* .idea/modules.xml
