---
title: What is the process for deleting an entry from the global git configuration?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: You can remove an entry in global configuration with git config --global --unset <key>.
---

**Contents**

[TOC]

### Removing Entries

1. List the global configuration entries with `git config --list --global`.
2. Identify the entry to be removed.
3. Unset the entry with `git config --global --unset <entry-name>`.

### Verifying Removal

1. List the global configuration entries again with `git config --list --global`.
2. Verify that the entry has been removed.
