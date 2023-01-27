---
title: How can I make 'git log' display filenames like 'svn log -v' does?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: Use the `--name-only` or `--name-status` options with `git log` to show filenames like `svn log -v`.
---

**Contents**

[TOC]

1. Install `git-svn`
   - `git-svn` is a Git command that allows you to use some Subversion features within Git. To install `git-svn`, use the following command:
   ```
   $ sudo apt-get install git-svn
   ```
2. Configure `git-svn` 
   - After installing `git-svn`, you need to configure it to work with your Subversion repository. To do this, use the following command:
   ```
   $ git svn init --stdlayout [svn-repository-url]
   ```
3. Use `git log` with `--name-status`
   - Once `git-svn` is installed and configured, you can use the `git log` command with the `--name-status` option to show filenames like `svn log -v`. The command should look like this:
   ```
   $ git log --name-status
   ```
4. Use `git log` with `--stat`
   - Alternatively, you can use the `git log` command with the `--stat` option to show filenames like `svn log -v`. The command should look like this:
   ```
   $ git log --stat
   ```
