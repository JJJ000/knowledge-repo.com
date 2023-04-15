---
title: What is the process for removing all of my docker images stored locally?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-30 00:00:00
updated_at: 2023-04-30 00:00:00
tldr: You can delete all local Docker images in Python by using the docker.client.api.remove\_image() method.
---

**Contents**

[TOC]

### Section 1: Install Docker SDK for Python

The first step in deleting all local Docker images in Python is to install the Docker SDK for Python. This can be done by running the following command in your terminal:

`pip install docker`

### Section 2: Connect to the Docker Daemon

Once the Docker SDK for Python is installed, you will need to connect to the Docker Daemon. This can be done by using the following code:

```
import docker

client = docker.from_env()
```

### Section 3: List All Images

Once you have connected to the Docker Daemon, you can list all the images that are currently stored locally. This can be done by using the following code:

```
images = client.images.list()
```

### Section 4: Delete All Images

Once you have a list of all the images stored locally, you can delete them all using the following code:

```
for image in images:
    client.images.remove(image.id)
```
