---
title: Creating a list of subscribers using mailchimp's API v3
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-15 00:00:00
updated_at: 2023-02-15 00:00:00
tldr: Using Mailchimp`s API v3 in Json, you can add subscribers to a list by making a POST request to the /lists/{list\_id}/members endpoint.
---

**Contents**

[TOC]

### Step 1: Create a POST Request

The first step is to create a POST request to the Mailchimp API endpoint. This request should include the list ID, the email address of the subscriber, and any other relevant subscriber information. The request should be formatted in JSON.

### Step 2: Send the Request

Once the request is created, it must be sent to the API endpoint. This can be done using an HTTP client such as cURL. The request should be sent with the appropriate authentication credentials.

### Step 3: Handle the Response

Once the request is sent, the API will respond with a status code and a message. If the request was successful, the status code will be 200 and the message will contain a confirmation that the subscriber was added.

### Step 4: Check the Subscriber List

Finally, the subscriber list should be checked to ensure that the subscriber was added correctly. This can be done by viewing the list in Mailchimp's dashboard or by making a GET request to the API.
