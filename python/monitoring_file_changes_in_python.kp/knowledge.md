---
title: What is the process for monitoring a file for modifications?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the watchdog library to monitor a file for changes in Python.
---

**Contents**

[TOC]

#1 Using Watchdog

Watchdog is a Python API library for monitoring file system events such as file creation, modification, and deletion. It is built on top of the native OS APIs, so it is highly efficient and can be used to monitor large numbers of files.

#2 Setting up Watchdog

Watchdog is available on PyPI and can be installed using pip:

```
pip install watchdog
```

#3 Writing a Script

Once Watchdog is installed, you can write a script to monitor a file for changes. The following example will watch a file called “example.txt” for changes and print out a message when it is modified:

```
import time
from watchdog.observers import Observer
from watchdog.events import FileSystemEventHandler

class MyHandler(FileSystemEventHandler):
    def on_modified(self, event):
        print("File Modified:", event.src_path)

observer = Observer()
observer.schedule(MyHandler(), path='example.txt', recursive=False)
observer.start()

try:
    while True:
        time.sleep(1)
except KeyboardInterrupt:
    observer.stop()
observer.join()
```

#4 Running the Script

Once the script is written, you can run it with Python:

```
python myscript.py
```

The script will start running in the background and will print out a message every time the “example.txt” file is modified.
