---
title: What gitignore rule is preventing my file from being tracked?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: The .gitignore file is containing the rule that is ignoring the specified file.
---

**Contents**

[TOC]

### Rule
The .gitignore file is a list of rules for ignoring files in a Git repository. The rule that is ignoring the file is the one that matches the file path.

### Syntax
The syntax for a .gitignore rule is a glob pattern. A glob pattern is a string that uses wildcard characters to match file paths. The wildcard characters are `*` for matching any number of characters, and `?` for matching any single character.

### Example
For example, if the file path of the file to be ignored is `src/main/java/MyClass.java`, the following rule would match it:

`src/main/java/*.java`

### Conclusion
By matching the file path with a glob pattern, the .gitignore file can be used to ignore certain files in a Git repository.
