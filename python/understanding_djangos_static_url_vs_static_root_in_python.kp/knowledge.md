---
title: What distinguishes static_url from static_root in django?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: STATIC\_URL is the URL prefix for static files, while STATIC\_ROOT is the absolute path to the directory where collectstatic will collect static files for deployment.
---

**Contents**

[TOC]

## Static files in Django
In Django, static files refer to any files (CSS, JS, images) that are served directly by the web server for rendering the website. Django provides a built-in system for managing static files in your projects, which includes two main settings: `STATIC_URL` and `STATIC_ROOT`.

## STATIC_URL
`STATIC_URL` refers to the base URL used for static files, which is usually `/static/`. This setting tells Django which URL pattern should be used to access static files in your project. For example, if you have a CSS file named `styles.css` stored in your static files directory, the URL to access it would be `http://yourdomain.com/static/styles.css`.

## STATIC_ROOT
`STATIC_ROOT` refers to the absolute file path to the directory where all the static files will be collected into a single directory. When the `collectstatic` command is run, Django gathers all the static files from each of your installed apps’ static directories, as well as any static directories defined in your project’s `STATICFILES_DIRS` setting, and places them in this directory. This is useful for overriding static files in third-party apps or libraries.

## Conclusion
In short, `STATIC_URL` is the base URL where Django will look for static files at runtime, while `STATIC_ROOT` is the absolute file path where static files will be collected using the `collectstatic` command. One is used in the code, and the other is used for running commands that collect static files into a single directory.
