---
title: How to post a JSON object containing an array using curl
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use the -d flag with your JSON object and array in quotation marks to send a PUT request with curl.
---

**Contents**

[TOC]

# Section 1: Setup

1. Create a file with the JSON object with an array.

2. Make sure the JSON is properly formatted and valid.

# Section 2: Execute the PUT Request

1. Open a terminal window and navigate to the directory containing the JSON file.

2. Execute the following command to make the PUT request:

`curl -X PUT -H "Content-Type: application/json" -d @<filename>.json <url>`

# Section 3: Verify the Request

1. Check the response code to verify that the request was successful.

2. Verify that the data was correctly updated in the database.

# Section 4: Cleanup

1. Delete the JSON file from the directory.
