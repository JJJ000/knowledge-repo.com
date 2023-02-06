---
title: What is the procedure for removing .orig files from a git repository after a merge?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Run `git clean -f -e *.orig` to delete all .orig files from the repository.
---

**Contents**

[TOC]

1. Using `git` Command

- Change to the directory with the `.orig` files
- Execute the command `git clean -f`

2. Using `find` Command

- Change to the directory with the `.orig` files
- Execute the command `find . -name '*.orig' -delete`

3. Using `rm` Command

- Change to the directory with the `.orig` files
- Execute the command `rm -f *.orig`

4. Using `bash` Script

- Create a `bash` script to search for `.orig` files and delete them
- Execute the script in the directory with the `.orig` files
