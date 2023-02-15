---
title: What is the best way to configure the default options for system.text.json.jsonserializer on a global level?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-15 00:00:00
updated_at: 2023-02-15 00:00:00
tldr: Default options for System.Text.Json.JsonSerializer can be set using the JsonSerializerOptions.Default property.
---

**Contents**

[TOC]

##### Setting Default Options

1. Create an instance of System.Text.Json.JsonSerializerOptions and set the desired options.

2. Call System.Text.Json.JsonSerializer.SetDefaultOptions and pass in the options instance.

##### Applying Options to All Serialization Operations

1. Create an instance of System.Text.Json.JsonSerializerOptions and set the desired options.

2. Create an instance of System.Text.Json.JsonSerializer and pass in the options instance.

3. Use the created JsonSerializer instance for all serialization operations.
