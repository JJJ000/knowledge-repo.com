---
title: Converting protobuf to JSON in python
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: The google.protobuf.json\_format module can be used to convert protobuf messages to JSON format in Python.
---

**Contents**

[TOC]

### Section 1: Prerequisites

- Python 3.x
- pip package manager
- protobuf library

### Section 2: Installation

To install the protobuf library, use the following command:

```
pip install protobuf
```

### Section 3: Usage

To convert protobuf to json, use the following code:

```
from google.protobuf.json_format import MessageToJson

# load protobuf message
message = ...

# convert to json
json_string = MessageToJson(message)
```

### Section 4: Output

The output of the above code will be a json string representing the protobuf message.
