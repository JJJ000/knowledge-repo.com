---
title: What is the reason behind git revert's complaint about the lack of a -m option?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Git revert requires the -m option to specify which parent commit to revert to.
---

**Contents**

[TOC]

# Overview

Git revert is a command used to undo changes made to a repository. When this command is used without the -m option, git will complain about it being missing. This is because the -m option is required for git revert to properly undo the changes and restore the repository to its previous state.

# Explanation

The -m option is used to specify the commit message that will accompany the revert. This message is used to explain why the changes were reverted and to document the change in the repository's history. Without the -m option, git revert cannot properly document the change and will therefore complain about the option being missing.

# Conclusion

In conclusion, the -m option is required for git revert to properly undo the changes and restore the repository to its previous state. Without the -m option, git revert will complain about it being missing.
