---
title: Duplicate a private git repository using a dockerfile
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Clone a private git repo with dockerfile by running the `git clone` command with the appropriate authentication credentials.
---

**Contents**

[TOC]

#Section 1: Prerequisites

Before attempting to clone a private git repo with a Dockerfile, there are some prerequisites that you must have in order to ensure a successful clone. 

1. You must have a valid GitHub account with access to the private repo.
2. You must have a Docker account with access to the private repo.
3. You must have Docker installed on your machine.

#Section 2: Cloning the Repo

Once you have the prerequisites in place, you can begin the process of cloning the private repo with the Dockerfile. 

1. Log in to your GitHub account and navigate to the private repo you wish to clone. 
2. Click the “Clone or download” button, and copy the URL of the repo.
3. Log in to your Docker account and navigate to the private repo you wish to clone. 
4. Click the “Clone or download” button, and copy the URL of the repo.
5. Open a terminal window and enter the command `git clone <repo-url>` to clone the repo.

#Section 3: Building the Docker Image

Once the repo has been successfully cloned, you can begin the process of building the Docker image.

1. Navigate to the cloned repo directory in the terminal window.
2. Enter the command `docker build -t <image-name> .` to build the Docker image.
3. Enter the command `docker images` to view the newly built image.

#Section 4: Running the Docker Image

Once the Docker image has been built, you can begin the process of running the image.

1. Enter the command `docker run -it <image-name>` to run the image.
2. Enter the command `docker ps` to view the running container.
3. Enter the command `docker exec -it <container-name> bash` to access the container.
