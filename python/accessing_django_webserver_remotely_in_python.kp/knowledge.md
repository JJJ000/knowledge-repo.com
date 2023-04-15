---
title: What is the procedure to reach the django webserver located locally from the global network?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: You can access the local Django webserver from outside world by using the public IP address and port number of the computer running the server.
---

**Contents**

[TOC]

## Introduction

By default, the Django web server runs on the local machine, which means it can only be accessed from the same computer. However, there are situations where you might need to access your local Django web server from the outside world, for example, testing webhook endpoints, showing a demo to a client or team member, or sharing your application with the public.

In this tutorial, we will explore various ways to access the local Django web server from the outside world.


## Prerequisites

Before we start, make sure you have the following:

- Django installed on your local machine
- A running Django web server
- A computer or device with access to the internet


## Using Ngrok

One of the easiest ways to access your local Django web server from the outside world is by using Ngrok. Ngrok is a tool that creates a secure tunnel between your local machine and a public endpoint, allowing you to expose your local development server to the internet.

To use Ngrok:

1. Download Ngrok from the official website.
2. Unzip the downloaded file and move the ngrok executable to a directory in your system path.
3. Start the Django development server by running `python manage.py runserver`
4. Open a new terminal window and navigate to the directory where you installed Ngrok.
5. Run `ngrok http 8000` to start a tunnel to your local Django development server.
6. Ngrok will generate a unique URL that you can use to access your local Django web server from the outside world.


## Using Port Forwarding

Another way to access your local Django web server from the outside world is by using port forwarding. Port forwarding allows you to redirect traffic from a specific port on your router to a specific port on your local machine.

To use port forwarding:

1. Log in to your router's configuration page.
2. Find the port forwarding settings in your router's configuration page.
3. Add a new rule that redirects traffic from an external port (e.g., 80) to the port that your Django development server is running on (e.g., 8000).
4. Create a static IP address for your machine. This ensures that your router always forwards traffic to the right machine, even if your local IP address changes.
5. Save your changes and restart your router if necessary.
6. You can now access your local Django web server by visiting your router's IP address followed by the external port you specified (e.g., http://192.168.1.1:80).


## Using Virtual Private Network (VPN)

If you have a Virtual Private Network (VPN) setup, you can use it to access your local Django web server from the outside world. A VPN is a private network that creates a secure connection between your local machine and a remote server, allowing you to access resources on that network as if you were physically there.

To use a VPN:

1. Connect to your VPN network.
2. Start the Django development server by running `python manage.py runserver`
3. Open a web browser on a remote machine and navigate to your Django web server's IP address (e.g., http://192.168.1.100:8000).
4. If your VPN is configured correctly, you should be able to access your local Django web server from the outside world.


## Conclusion

In this tutorial, we explored various ways to access the local Django web server from the outside world. Each method has its pros and cons, depending on the situation. Use Ngrok if you want a quick and easy way to share your application with others. Use port forwarding if you want a more permanent solution. Use VPN if you want a secure way to access your local Django web server remotely.
