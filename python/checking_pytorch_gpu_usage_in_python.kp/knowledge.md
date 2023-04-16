---
title: What is the procedure for verifying that pytorch is utilizing the gpu?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can check if PyTorch is using the GPU by running `torch.cuda.is\_available()`.
---

**Contents**

[TOC]

# Section 1: Check if a GPU is Available

The simplest way to check if a GPU is available is to use the `torch.cuda.is_available()` function. This function will return True if a GPU is available and False if not.

# Section 2: Check if a GPU is Being Used

To check if a GPU is being used by PyTorch, you can use the `torch.cuda.current_device()` function. This function will return the index of the GPU being used by PyTorch. If the index is -1, then no GPU is being used.

# Section 3: Check Which GPU is Being Used

If you want to know which GPU is being used by PyTorch, you can use the `torch.cuda.get_device_name()` function. This function will return the name of the GPU being used by PyTorch.

# Section 4: Check GPU Memory Usage

Finally, to check how much GPU memory is being used by PyTorch, you can use the `torch.cuda.memory_allocated()` function. This function will return the amount of GPU memory allocated by PyTorch in bytes.
