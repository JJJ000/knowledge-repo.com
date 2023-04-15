---
title: How can git be used to manage crlf (carriage return, line feed)?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Git`s core.autocrlf setting should be configured to ensure that line endings are properly handled.
---

**Contents**

[TOC]

1. **Git Configuration:**
   Git can be configured to automatically convert CRLF line endings to LF when committing code. This can be done by setting the `core.autocrlf` config option to `true`.

2. **Line Ending Conversion:**
   If `core.autocrlf` is not set to `true`, then CRLF line endings can be converted manually using the `git config --global core.autocrlf input` command.

3. **Checking Line Endings:**
   To check if the line endings have been converted correctly, run the `git diff --check` command. This command will output any differences between the LF and CRLF line endings.

4. **Preventing CRLF Issues:**
   To prevent CRLF issues in the first place, it is best practice to set the `core.autocrlf` config option to `true` and configure the editor to save files with LF line endings.
