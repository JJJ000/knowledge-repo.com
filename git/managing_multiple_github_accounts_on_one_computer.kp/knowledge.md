---
title: Can I have more than one github account on the same computer?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Yes, multiple GitHub accounts can be used on the same computer by setting up different SSH keys for each account.
---

**Contents**

[TOC]

### Set Up SSH Keys

The first step to managing multiple GitHub accounts on the same computer is to set up separate SSH keys for each account. SSH keys provide a secure way to authenticate with GitHub and are necessary for using the command line to interact with GitHub repositories. To set up an SSH key for a GitHub account, follow the steps outlined in GitHub's documentation.

### Configure Git

Once SSH keys have been set up for each account, the next step is to configure Git to use the appropriate SSH key for each account. This can be done by editing the `~/.ssh/config` file and adding a section for each account with the appropriate Host and IdentityFile settings.

### Create Aliases

To make it easier to switch between accounts, aliases can be created for each account. This can be done by editing the `~/.bash_profile` file and adding a line for each alias. For example, if the username for the first account is `user1`, the line `alias user1="git config user.name 'User1'"` can be added to the `~/.bash_profile` file.

### Use Aliases

Once the aliases have been created, they can be used to switch between accounts. To do so, open a new terminal window and type the alias for the desired account. For example, if the alias for the first account is `user1`, typing `user1` in the terminal window will switch to that account.
