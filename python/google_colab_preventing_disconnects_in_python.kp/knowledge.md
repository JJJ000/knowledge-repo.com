---
title: Is there a way to avoid google colab from getting disconnected?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To prevent Google Colab from disconnecting, use a script to continuously perform an action such as printing the current time or running a loop that performs calculations.
---

**Contents**

[TOC]

## 1. Increase idle timeout

Google Colab will disconnect if there is no activity for a certain amount of time. This can be annoying if you are working on a long project or need to leave your session running for an extended period. One way to prevent this is to increase the idle timeout length. This can be done using the `jupyter_http_over_ws` package.

```
!pip install jupyter_http_over_ws
!jupyter serverextension enable --py jupyter_http_over_ws
!jupyter notebook --NotebookApp.allow_origin='https://colab.research.google.com' --port=8888 --NotebookApp.port_retries=0
```

After running these commands, a link will be generated. Open the link in a new tab, and it will connect to your Colab session.

## 2. Keep the browser window open

Another way to prevent Google Colab from disconnecting is to keep the browser window open. If you don't interact with the notebook, Colab will disconnect after a certain amount of time. However, if you keep the browser window open, Colab will remain connected. 

## 3. Use a Chrome extension

There are several Chrome extensions that can help prevent Google Colab from disconnecting. Some popular ones include:

- [Auto Refresh Plus](https://chrome.google.com/webstore/detail/auto-refresh-plus/oilipfekkmncanaajkapbpancpelijih?hl=en)
- [Super Auto Refresh](https://chrome.google.com/webstore/detail/super-auto-refresh-plus/globgafddkdlnalejlkcpaefakkhkdoa?hl=en)

These extensions can be set up to automatically refresh the Colab page every few minutes, which will prevent it from disconnecting.

## 4. Use GPU/TPU

If you are using the GPU/TPU runtime in Colab, your session may stay connected for a longer period of time. This is because Colab needs to keep the hardware resources allocated to your session, which can keep it from disconnecting. However, this isn't always a feasible solution, as the GPU/TPU runtime is only available for a limited amount of time per day.
