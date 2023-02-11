---
title: Sending a JSON object with nested elements using httpie
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: Send the nested JSON object using HTTPie by using the `--json` flag.
---

**Contents**

[TOC]

# Section 1: Install HTTPie

HTTPie is a command line HTTP client that allows you to make HTTP requests from the command line. It is available for download on GitHub.

# Section 2: Create the JSON Object

Create a JSON object that contains the nested data you would like to send. For example, if you wanted to send a nested JSON object containing the names of two people, you could create the following JSON object:

```json
{
  "person1": {
    "name": "John Doe"
  },
  "person2": {
    "name": "Jane Doe"
  }
}
```

# Section 3: Send the Request

Once you have created the JSON object, you can use HTTPie to send the request. You can use the `--json` flag to specify that the data is in JSON format. For example, if you wanted to send the above JSON object, you could run the following command:

```
http --json POST http://example.com/data person1.name=John\ Doe person2.name=Jane\ Doe
```

# Section 4: Verify the Request

Once the request has been sent, you can use the response to verify that the data was sent correctly. For example, if the response contains the names of the two people you sent in the request, then you can be sure that the request was successful.
