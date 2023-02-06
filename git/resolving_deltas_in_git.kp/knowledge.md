---
title: What is git doing when it says it is "calculating differences" or "comparing changes"?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Git is comparing the differences between two versions of a file and combining them into a single updated version.
---

**Contents**

[TOC]

**Git Deltas**

Git deltas are the differences between two versions of a file. When a file is changed, rather than storing the entire new file, git stores the differences between the two versions as a delta.

**Delta Compression**

Git uses delta compression to store deltas. Delta compression is a technique used to store the differences between two versions of a file in a compact form. This allows git to store changes to a file without having to store the entire file each time.

**Resolving Deltas**

When git is resolving deltas, it is taking the stored deltas and reconstructing the original file. This is done by taking the original version of the file, and then applying the stored deltas to it. This allows git to quickly reconstruct the original file without having to store the entire file each time.

**Conclusion**

Git is able to store changes to a file efficiently by using delta compression to store the differences between two versions of a file. When git is resolving deltas, it is taking the stored deltas and reconstructing the original file.
