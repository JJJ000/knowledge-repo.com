---
title: What is the process for setting my preferred editor for writing git commit messages?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Set the `GIT_EDITOR` environment variable to the path of the editor of your choice.
---

**Contents**

[TOC]

### Check the Default Editor

Before you try to change the default editor, it is important to check what the current default editor is. To do this, you can run the command `git config --global core.editor` in your terminal.

### Set the Default Editor

To set the default editor for git, you can run the command `git config --global core.editor <editor>`, where `<editor>` is the command used to invoke your editor of choice. For example, if you want to use Vim as your editor, you would run `git config --global core.editor vim`.

### Verify the Change

Once you have set the default editor, you can verify that it has been changed by running the command `git config --global core.editor` again. This should return the command you used to set the editor.

### Test the Editor

Finally, you can test that the editor has been set correctly by running `git commit` in your terminal. This should open your editor of choice, allowing you to enter your commit message.
