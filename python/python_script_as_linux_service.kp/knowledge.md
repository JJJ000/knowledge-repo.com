---
title: What are the steps to run a Python script as a service or daemon in linux?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use a process manager like systemd or Supervisor to run the Python script as a service or daemon in Linux.
---

**Contents**

[TOC]

## Section 1: Introduction

In Linux, services or daemons are programs that run in the background without any user interaction. Python scripts can also be turned into services or daemons that can run persistently in the system. In this guide, we will see how to make a Python script run as a service or daemon in Linux.

## Section 2: Creating a Python Script as a Service

To create a Python script as a service, we need to create a systemd service file. Systemd is a system and service manager that replaces System V init as the default init system used by many Linux distributions. The systemd service file is responsible for defining the properties of a service.

Here are the steps to create a Python script as a service:

1. Create a file named `<servicename>.service` in the `/etc/systemd/system/` directory. Replace <servicename> with the name of your service.

```console
sudo nano /etc/systemd/system/<servicename>.service
```

2. Add the following lines to the service file:

```
[Unit]
Description=<service description>

[Service]
ExecStart=<path to python> <path to script>
WorkingDirectory=<working directory>
Restart=always
User=<username>

[Install]
WantedBy=multi-user.target
```

Here is what each line represents:

- `[Unit]` section defines the description of the service.
- `[Service]` section defines the execution properties of the service.
- `ExecStart` specifies the path to the Python interpreter and the path to the Python script.
- `WorkingDirectory` specifies the path to the working directory of the script.
- `Restart` specifies when the service should be restarted (always, on-failure, etc).
- `User` specifies the user account that the service should run under.
- `[Install]` section defines the dependencies and target for the service.

3. Save and close the file.

4. Reload the systemd daemon to load the new service.

```console
sudo systemctl daemon-reload
```

5. Start the service.

```console
sudo systemctl start <servicename>
```

The Python script will now run as a service.

## Section 3: Checking the Status and Logs of the Service

To check the status of the service, use the `systemctl status` command.

```console
sudo systemctl status <servicename>
```

To view the logs of the service, use the `journalctl` command.

```console
sudo journalctl -u <servicename>
```

## Section 4: Enabling and Disabling the Service

To enable the service to start at boot, use the `systemctl enable` command.

```console
sudo systemctl enable <servicename>
```

To disable the service from starting at boot, use the `systemctl disable` command.

```console
sudo systemctl disable <servicename>
```

These commands only modify the symbolic links in the `/etc/systemd/system/multi-user.target.wants/` directory. To remove the service completely, delete the service file and reload the systemd daemon.

```console
sudo rm /etc/systemd/system/<servicename>.service
sudo systemctl daemon-reload
```
