---
title: How can I use a gpg key to automatically sign commits in git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Yes, you can use the git commit -S flag to autosign commits with a GPG key.
---

**Contents**

[TOC]

### Generating a GPG Key

In order to use a GPG key to sign commits in Git, the first step is to generate the GPG key. This can be done using the command `gpg --gen-key` on a terminal. This command will prompt the user to enter some information, such as name, email address, and a passphrase. Once the information is entered, the GPG key will be generated.

### Configuring Git to Use GPG Key

Once the GPG key is generated, it needs to be configured in Git. This can be done by running the command `git config --global user.signingkey <key_id>`, where `<key_id>` is the ID of the generated GPG key. This command will configure Git to use the GPG key for signing commits.

### Signing Commits with GPG Key

Once the GPG key has been configured in Git, it can be used to sign commits. This can be done by running the command `git commit -S -m <message>`, where `<message>` is the commit message. This will sign the commit with the GPG key configured in Git.

### Automatically Signing Commits

In order to automatically sign commits with the GPG key, the `commit.gpgsign` configuration option needs to be set to true. This can be done by running the command `git config --global commit.gpgsign true`. This will configure Git to automatically sign commits with the GPG key configured in Git.
