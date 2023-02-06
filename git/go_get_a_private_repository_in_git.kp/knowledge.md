---
title: How can I access a private repository?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: The proper way to `go get` a private repository in Git is to clone it using the SSH or HTTPS URL of the repository.
---

**Contents**

[TOC]

1. **Clone the Repository**

To start, you need to clone the repository. This will create a local copy of the repository on your computer. To do this, you need to enter the following command in your terminal: 
`git clone <repo_url>`

2. **Add the SSH Key to the Repository**

Next, you need to add your SSH key to the repository. This will allow you to securely access the repository without having to enter your credentials each time. To do this, you need to enter the following command in your terminal: 
`ssh-add <path_to_your_private_key>`

3. **Configure the SSH Key**

Once you have added your SSH key to the repository, you need to configure it. To do this, you need to enter the following command in your terminal: 
`git config --global user.name "<username>"`

4. **Pull the Repository**

Finally, you need to pull the repository. This will download the latest version of the repository to your local copy. To do this, you need to enter the following command in your terminal: 
`git pull <repo_url>`
