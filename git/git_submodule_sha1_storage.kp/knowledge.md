---
title: What location does git save the sha1 hash of the commit for a submodule?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Git stores the SHA1 of the commit for a submodule in the .gitmodules file.
---

**Contents**

[TOC]

1. Submodule Repository 
   Git stores the SHA1 of the commit for a submodule in the submodule repository. 

2. Working Tree 
   The SHA1 of the commit is also stored in the working tree of the parent repository.

3. Index 
   The SHA1 of the commit is also stored in the index of the parent repository.

4. Config File 
   The SHA1 of the commit is also stored in the config file of the parent repository.
