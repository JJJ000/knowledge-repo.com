---
title: The action of retrieving environment variables from a file that specifies the environment
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Use the `dotenv` package to load environment variables from a file named `.env` located in the same directory as the Python script.
---

**Contents**

[TOC]

## Introduction

Environment variables are a ubiquitous way of passing configuration information between programs or processes. Often, Python applications will rely on environment variables to control aspects of their behavior, such as database connection strings or API keys. In this tutorial, we will cover how to read environment variables from an environment file in Python.

## Creating an Environment File

Before we can read environment variables from a file in Python, we first need to create an environment file. An environment file is simply a plain text file that contains key-value pairs of environment variables. Here is an example environment file:

```
DATABASE_URL=postgres://user:password@localhost:5432/mydatabase
API_KEY=foobar
```

In this example, we have two environment variables defined: a `DATABASE_URL` and an `API_KEY`. The `DATABASE_URL` is a connection string for a Postgres database, and the `API_KEY` is a secret key for accessing an API.

## Reading Environment Variables from a File

Once we have created our environment file, we can read the environment variables into our Python script using the `dotenv` library. 

First, we need to install the `dotenv` library:

```
pip install python-dotenv
```

Then, we can load the environment variables from our file using the following code:

```python
import os
from dotenv import load_dotenv

# Load environment variables from .env file
load_dotenv()

# Access environment variables
db_url = os.getenv("DATABASE_URL")
api_key = os.getenv("API_KEY")
```

In this code, we first import the `os` module and the `load_dotenv` function from the `dotenv` library. We then call `load_dotenv()` to load the environment variables from the file named `.env` in the current working directory. Finally, we use `os.getenv()` to access the environment variables by name.

## Conclusion

In this tutorial, we covered how to read environment variables from an environment file in Python. We first created an example environment file, and then used the `dotenv` library to load the variables into our script. With this technique, we can easily manage configuration variables and secrets in a secure and organized way.
