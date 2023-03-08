---
title: Is it possible for me to include a message in the tqdm progress bar?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Yes, you can add a message to the tqdm progress bar by setting the desc parameter.
---

**Contents**

[TOC]

Yes, you can add a message to the tqdm progress bar in Python. There are several ways to do this, depending on your specific needs and the version of tqdm that you are using. The following sections will outline some of the most common methods for adding a message to a tqdm progress bar.

### Using the 'desc' Parameter

One simple way to add a message to a tqdm progress bar is to use the 'desc' parameter when creating the progress bar. This parameter allows you to specify a custom description that will be displayed alongside the progress bar. Here is an example:

```python
from tqdm import tqdm

for i in tqdm(range(100), desc="Processing..."):
    # do some work here
```

In this example, the progress bar will be created with the label "Processing..." displayed above it. As the loop iterates, the progress bar will update and the label will remain constant.

### Using the 'set_description' Method

If you need to update the message associated with a tqdm progress bar during the execution of your code, you can use the 'set_description' method. This method allows you to set a new message for the progress bar without interrupting the progress updates. Here is an example:

```python
from tqdm import tqdm
import time

pbar = tqdm(range(100))
for i in pbar:
    pbar.set_description("Processing item %d" % i)
    time.sleep(0.1)
```

In this example, the progress bar is created outside of the loop and then updated inside the loop using the 'set_description' method. Each time the method is called, the message associated with the progress bar will be updated with the new value.

### Using the 'write' Method

If you need to add a message to a progress bar that is not associated with any particular iteration of a loop, you can use the 'write' method. This method allows you to print a message to the console that will be displayed alongside the progress bar. Here is an example:

```python
from tqdm import tqdm
import time

pbar = tqdm(range(100))
pbar.write("Starting processing...")
for i in pbar:
    # do some work here
```

In this example, the 'write' method is used to display a message before the progress bar is created. This message will be displayed in the console next to the progress bar, and will remain on the screen even after the progress updates begin.
