---
title: What steps can I take to resolve the git error "object file ... is empty"?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Run `git gc` to clean up empty objects and reclaim disk space.
---

**Contents**

[TOC]

### Check File Contents

The first step to resolving this error is to check the contents of the file referenced in the error. This can be done by running `git cat-file -p <object-hash>` in the command line, where `<object-hash>` is the object hash that appears in the error message. This will show the contents of the object file.

If the file is empty, then the file must be replaced.

### Replace File

The second step is to replace the empty file. This can be done by running `git hash-object -w <filename>`, where `<filename>` is the name of the file that needs to be replaced. This command will create a new object file with the contents of the file specified.

### Update Reference

The third step is to update the reference to the new object file. This can be done by running `git update-ref <ref> <new-object-hash>`, where `<ref>` is the reference to the object file and `<new-object-hash>` is the new object hash that was generated when the file was replaced.

### Verify Changes

The fourth and final step is to verify that the changes have been made correctly. This can be done by running `git cat-file -p <new-object-hash>` again to check that the contents of the object file are correct.
