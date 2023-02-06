---
title: Git rebase --continue will still display a message even if all merge conflicts have been successfully resolved
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Git rebase --continue may still complain if there are unresolved changes in the index.
---

**Contents**

[TOC]

# Overview
Git rebase --continue will complain if there are still unresolved merge conflicts even after all merge conflicts have been resolved. This is because the rebase process is not yet complete, and the command needs to be run again to finish the rebase.

# Reasons
The main reason that Git rebase --continue complains even when all merge conflicts have been resolved is because the rebase process is not yet complete. The rebase process involves multiple steps, and each step needs to be completed in order for the rebase to be successful. If any of the steps are not completed, then the rebase process will fail and Git will complain.

# Solution
The solution is to run the Git rebase --continue command again after all merge conflicts have been resolved. This will complete the rebase process and allow the changes to be committed. It is important to remember to commit the changes after the rebase is complete, as this will ensure that the changes are saved and can be used in the future.
