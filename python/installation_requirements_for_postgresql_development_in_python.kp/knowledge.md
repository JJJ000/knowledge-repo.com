---
title: If you want to create a server-side extension, you will have to install postgresql-server-dev-x.y. alternatively, if you are developing a client-side application, libpq-dev needs to be installed
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: If you are building a server-side extension, you need to install postgresql-server-dev-X.Y, and if you are building a client-side application in Python, you need to install libpq-dev.
---

**Contents**

[TOC]

Installing postgresql-server-dev-X.Y

## Overview

Installing postgresql-server-dev-X.Y is necessary for building a server-side extension for PostgreSQL. It includes the necessary header files and libraries for building PostgreSQL extensions.

## Installation

1. Open your terminal.
2. Run the command: `sudo apt-get install postgresql-server-dev-X.Y` (replace X.Y with the version number you need).
3. Enter your password when prompted.
4. Wait for the installation to finish.

## Verification

To verify that postgresql-server-dev-X.Y is installed, do the following:

1. Open your terminal.
2. Run the command: `dpkg -l | grep postgresql-server-dev-X.Y` (replace X.Y with the version number you installed).
3. If postgresql-server-dev-X.Y is installed, it will be displayed in the output.

Installing libpq-dev

## Overview

Installing libpq-dev is necessary for building a client-side application in Python. It includes the necessary header files and libraries for building PostgreSQL applications.

## Installation

1. Open your terminal.
2. Run the command: `sudo apt-get install libpq-dev` .
3. Enter your password when prompted.
4. Wait for the installation to finish.

## Verification

To verify that libpq-dev is installed, do the following:

1. Open your terminal.
2. Run the command: `dpkg -l | grep libpq-dev` .
3. If libpq-dev is installed, it will be displayed in the output.
