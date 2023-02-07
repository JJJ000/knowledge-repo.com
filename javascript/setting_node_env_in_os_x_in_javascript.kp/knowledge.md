---
title: How can I change node_env to production/development in os x?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: In OS X, you can set the NODE\_ENV environment variable to either production or development by running the command `export NODE\_ENV=production/development` in the terminal.
---

**Contents**

[TOC]

# Section 1: Using Command Line

The most common way to set the NODE_ENV environment variable is to use the command line.

To set the NODE_ENV to production, type the following command in the terminal:

`export NODE_ENV=production`

To set the NODE_ENV to development, type the following command in the terminal:

`export NODE_ENV=development`

# Section 2: Using a Script

You can also set the NODE_ENV environment variable by writing a script.

To set the NODE_ENV to production, type the following command in the script:

`process.env.NODE_ENV = 'production';`

To set the NODE_ENV to development, type the following command in the script:

`process.env.NODE_ENV = 'development';`

# Section 3: Using Environment Variables

You can also set the NODE_ENV environment variable by setting an environment variable.

To set the NODE_ENV to production, type the following command in the terminal:

`export NODE_ENV=production`

To set the NODE_ENV to development, type the following command in the terminal:

`export NODE_ENV=development`

# Section 4: Using a Configuration File

You can also set the NODE_ENV environment variable by creating a configuration file.

Create a file called `.env` in the root directory of your project, and add the following line to it:

`NODE_ENV=production`

Or, if you want to set the NODE_ENV to development, add the following line to the `.env` file:

`NODE_ENV=development`
