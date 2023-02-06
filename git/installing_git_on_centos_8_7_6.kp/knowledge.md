---
title: What is the process for installing the most recent version of git on centos 8.x/7.x/6.x?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Run `yum install git` to install the latest version of git on CentOS 8.x/7.x/6.x.
---

**Contents**

[TOC]

### Step 1: Install Git

To install the latest version of Git on CentOS 8.x/7.x/6.x, you need to first install the EPEL (Extra Packages for Enterprise Linux) repository. This repository provides additional packages that are not included in the default CentOS package repository. To install the EPEL repository, run the following command:

```
sudo yum install epel-release
```

Once the EPEL repository is installed, you can install the latest version of Git using the following command:

```
sudo yum install git
```

### Step 2: Verify Installation

Once the installation is complete, you can verify the version of Git installed by running the following command:

```
git --version
```

The output of the command should look something like this:

```
git version 2.25.1
```

### Step 3: Configure Git

Now that Git is installed, you can configure it to use your name and email address. This information will be used to identify your commits. To configure these settings, run the following commands:

```
git config --global user.name "Your Name"
git config --global user.email "your_email@example.com"
```

### Step 4: Test Git

To test the installation, you can create a new repository and add a file. To do this, run the following commands:

```
mkdir test-repo
cd test-repo
git init
echo "Test file" > test.txt
git add test.txt
git commit -m "Initial commit"
```

If the commands execute without any errors, then your installation of Git is working correctly.
