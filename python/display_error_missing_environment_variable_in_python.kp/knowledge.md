---
title: The error '_tkinter.tclerror no display name and no $display environment variable' needs to be restated as there is no display name specified and no $display environment variable found in _tkinter.tclerror
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: The error occurs when trying to use a graphical user interface in Python without a proper display setup.
---

**Contents**

[TOC]

Section 1: Introduction
When working with graphical user interfaces (GUIs) using Python, it is common to use a library called Tkinter. However, when running Tkinter on a remote machine or in a headless environment, you may encounter an error with the message "_tkinter.TclError: no display name and no $DISPLAY environment variable". This error occurs because Tkinter requires an active display to function properly. Therefore, this error can be solved by setting up a display or by using a virtual display.

Section 2: Setting up a Display
One way to solve the _tkinter.TclError error is to set up a display. This can be achieved by logging into the machine using a GUI or remote desktop software, or by connecting a physical display to the machine. Once a display is active, running the Tkinter code should no longer produce the error.

Section 3: Using a Virtual Display
Another way to solve the _tkinter.TclError error is to use a virtual display. A virtual display can be set up using Xvfb (X virtual framebuffer). Xvfb is a display server that runs in memory and does not require a physical display. Once Xvfb is installed, it can be started with the command "Xvfb :0 -screen 0 1024x768x24 &", which will create a virtual display of 1024x768 pixels with a color depth of 24 bits on the display ":0". The Tkinter code can then be executed with the environment variable "DISPLAY=:0" set, which will direct the output to the virtual display.

Section 4: Conclusion
In conclusion, the _tkinter.TclError error can be solved by setting up a display or by using a virtual display. Setting up a display requires a physical display or a login through a GUI or remote desktop software, while setting up a virtual display requires installing Xvfb and running the command "Xvfb :0 -screen 0 1024x768x24 &", then executing the Tkinter code with the environment variable "DISPLAY=:0" set. With these solutions, Tkinter can be used even in headless environments or on remote machines.
