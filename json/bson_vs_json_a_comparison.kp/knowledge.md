---
title: What is the distinction between bson and json?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: BSON is a binary-encoded serialization of JSON-like documents that is more efficient and faster than JSON.
---

**Contents**

[TOC]

# What is BSON?
BSON (Binary JSON) is a binary-encoded serialization of JSON-like documents. BSON is designed to be lightweight, traversable, and efficient. It is a binary form of JSON that can be used to store data in a more efficient way than JSON.

# How is BSON different from JSON?
BSON is more efficient and compact than JSON. BSON is a binary representation of JSON documents and has a much smaller size than JSON when stored on disk or in memory. BSON also supports a wider range of data types than JSON, including integers, dates, and binary data. Additionally, BSON supports embedded documents and arrays, which allows for more complex data structures than JSON. Finally, BSON supports a number of advanced query operators, such as $gt, $lt, and $regex, which allow for more powerful querying than JSON.
