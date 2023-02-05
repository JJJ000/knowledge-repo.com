---
title: What steps do I need to take to run flask on port 80?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Set the port parameter to 80 when running the Flask app.
---

**Contents**

[TOC]

# Step 1: Install Apache

In order to run Flask on port 80, you need to install the Apache web server. Apache is an open-source web server that allows you to run Flask applications on port 80.

# Step 2: Configure Apache

Once Apache is installed, you need to configure it to run Flask on port 80. This can be done by editing the Apache configuration file, usually located at /etc/apache2/httpd.conf. You need to add the following lines to the configuration file:

LoadModule wsgi_module modules/mod_wsgi.so

WSGIScriptAlias / /path/to/flask/application.wsgi

# Step 3: Start Apache

Once Apache is configured, you need to start it. This can be done by running the following command:

sudo apachectl start

# Step 4: Access Flask Application

Once Apache is running, you can access your Flask application by going to http://localhost:80. You should now be able to see your Flask application running on port 80.
