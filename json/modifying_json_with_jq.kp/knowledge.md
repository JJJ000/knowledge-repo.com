---
title: Edit a key-value pair in a JSON file using jq in its original location
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Yes, it is possible to modify a key-value in a JSON using jq in-place by using the `-i` or `--in-place` flag.
---

**Contents**

[TOC]

1. Install jq

In order to modify a key-value in a json file using jq, you must first install jq. jq can be installed on Linux, Mac, and Windows.

2. Modify Key-Value

Once jq is installed, you can modify a key-value in a json file using the following command:

`jq '.key=value' --arg key value --argjson value value filename.json > filename_modified.json`

Where `key` and `value` are the key and value of the key-value pair you want to modify.

3. In-Place Modification

If you want to modify the json file in-place, you can use the `-i` or `--in-place` option. This will overwrite the original json file with the modified version.

`jq '.key=value' --arg key value --argjson value value -i filename.json`

4. Output

After running the command, the modified json file will be saved in the same location as the original json file.
