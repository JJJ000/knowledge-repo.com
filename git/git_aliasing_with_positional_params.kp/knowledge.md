---
title: Creating aliases in git using positional parameters
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: A git alias can be used to create a custom command that takes positional parameters as arguments.
---

**Contents**

[TOC]

### What are Git Aliases?
Git aliases are shortcuts that can be used to quickly execute a series of Git commands. They are created using the `git config` command and can be used to save time and simplify common tasks.

### What are Positional Parameters?
Positional parameters are arguments that are passed to a command, and their order is important. For example, when using the `git checkout` command, the positional parameters are the branch name, and the command will fail if the parameters are in the wrong order.

### Git Alias with Positional Parameters
Git aliases can be used with positional parameters. For example, the following alias will check out a branch with the name specified as the first argument:

```git
git config --global alias.co 'checkout $1'
```

This alias can then be used by typing `git co <branch_name>`. The argument `$1` will be replaced with the branch name specified.

### Conclusion
Git aliases can be used to quickly and easily execute common tasks. They can also be used with positional parameters, which allows for more flexibility and customization when executing commands.
