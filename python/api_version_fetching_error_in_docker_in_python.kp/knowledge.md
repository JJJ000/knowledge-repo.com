---
title: An exception was encountered in docker stating that there was an error in retrieving the server's API version
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: The error message suggests that there is an issue with connecting to the Docker API to retrieve its version in a Python script.
---

**Contents**

[TOC]

# Introduction
If you are trying to use the Docker API to interact with Docker using Python, you may come across the following error: `docker.errors.DockerException: Error while fetching server API version`. This error is common when trying to run Python scripts that use the Docker API but it can also occur when trying to run Docker commands in the command line. In this article, we will explore the potential causes of this error and how to fix them.

# Reasons for the Error
The `docker.errors.DockerException: Error while fetching server API version` error is caused by the inability of the Docker client to connect to the Docker daemon. There are several reasons why the client might fail to connect to the daemon. Here are some of the most common:

## 1. Docker daemon is not running
Before you can use the Docker API, the Docker daemon must be running. If the Docker daemon is not running on your system, the client will not be able to connect to it and you will get the `docker.errors.DockerException: Error while fetching server API version` error. To fix this, you should start the Docker daemon by running the following command in the terminal:

```
sudo service docker start
```

## 2. Docker daemon is not reachable
If the Docker daemon is running but the client still can't connect to it, it's possible that the daemon is not reachable due to a network or firewall issue. Check that your network is working properly and that any firewalls are not blocking Docker's network ports. Typically, Docker uses port 2375 for unencrypted connections and port 2376 for encrypted connections.

## 3. Docker API version is not compatible
The `docker.errors.DockerException: Error while fetching server API version` error can occur when the Docker client and daemon are using different versions of the API. This can happen if you have updated one component without updating the other. To fix this, you should update both the Docker client and daemon to the same version by running the following commands:

### Update Docker client
```
sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io
```

### Update Docker daemon
```
sudo service docker stop
sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io
sudo service docker start
```

## 4. Docker API is not accessible
If the Docker daemon is running and reachable but the API is still not accessible, it's possible that the API has been disabled or restricted. Check that the API is enabled and that you have the necessary permissions to access it. By default, Docker's API is only accessible to the root user and members of the docker group. If you are not a member of the docker group, you can add yourself by running the following command:

```
sudo usermod -aG docker <your_username>
```

# Conclusion
The `docker.errors.DockerException: Error while fetching server API version` error can be caused by several factors, including a non-running daemon, network or firewall issues, version conflicts, and API restrictions. By following the steps outlined in this article, you should be able to fix the issue and start using the Docker API in your Python scripts.
