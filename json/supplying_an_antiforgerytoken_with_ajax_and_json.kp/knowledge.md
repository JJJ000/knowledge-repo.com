---
title: What is the best way to include an antiforgerytoken when sending JSON data with $.ajax?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: Include the token in the request payload as a property of the JSON data.
---

**Contents**

[TOC]

## Step 1: Generate AntiForgeryToken

The first step is to generate an AntiForgeryToken. This can be done by adding the following code to the view:

```
@Html.AntiForgeryToken()
```

This will generate a token that will be stored in a hidden field in the view.

## Step 2: Include AntiForgeryToken in JSON

The second step is to include the AntiForgeryToken in the JSON data that is sent to the server. This can be done by adding the following code to the JavaScript:

```
var token = $('input[name="__RequestVerificationToken"]').val();
var data = {
    __RequestVerificationToken: token,
    // other data
};
```

This will add the token to the JSON data that is sent to the server.

## Step 3: Validate AntiForgeryToken on Server

The third step is to validate the AntiForgeryToken on the server. This can be done by adding the following code to the controller action:

```
[ValidateAntiForgeryToken]
public ActionResult MyAction(MyModel model)
{
    // code
}
```

This will validate the token and ensure that the request is coming from a trusted source.

## Step 4: Handle Token Validation Failure

The fourth step is to handle the case when the token validation fails. This can be done by adding the following code to the controller action:

```
[ValidateAntiForgeryToken]
public ActionResult MyAction(MyModel model)
{
    if (!ModelState.IsValid)
    {
        return new HttpStatusCodeResult(HttpStatusCode.Forbidden);
    }
    
    // code
}
```

This will return a 403 Forbidden status code if the token validation fails.
