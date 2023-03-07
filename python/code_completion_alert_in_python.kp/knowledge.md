---
title: Trigger an alarm upon completion of the code
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: You can use the winsound module to play a sound file after the code finishes executing.
---

**Contents**

[TOC]

## Introduction

As an AI language model, I do not have the capability to sound an alarm when a Python code finishes executing. However, I can suggest various ways in which you, as a human user or programmer, can achieve this functionality.

## Using beeps in Python

Python provides a simple way to generate a beep sound using the `winsound` module. You can use this module to create a beep sound when your Python code completes.

```python
import winsound

# Your code

winsound.Beep(1000, 500)  # frequency in Hz and duration in ms
```

The `Beep` function takes two arguments: the frequency in Hz and the duration in milliseconds. You can customize the frequency and duration to produce different sounds.

## Using a media player

You can also use a media player, such as VLC or Windows Media Player, to play a sound when your Python code finishes. Here is an example of how to do this using VLC player:

```python
import os

# Your code

os.system("vlc --play-and-exit sound.mp3")
```

The `os.system` function runs a command in the shell. In this case, it uses the VLC player to play a sound file (`sound.mp3`) and then exits.

## Using notifications

You can also use desktop notifications to alert you when your Python code finishes. Here is an example using the `plyer` module:

```python
from plyer import notification

# Your code

notification.notify(
    title="Code Finished",
    message="Your Python code has completed.",
    app_name="Python"
)
```

The `notification.notify` function creates a desktop notification with a title, message, and app name. You can customize the content of the notification to suit your needs.

## Conclusion

In this article, we explored three ways to sound an alarm when your Python code finishes executing. You can use beeps, media players, or desktop notifications to achieve this functionality.
