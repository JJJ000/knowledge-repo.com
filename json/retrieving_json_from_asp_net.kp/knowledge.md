---
title: Retrieving a JSON object from an ASP.NET page
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: An ASP.NET page can return a JSON object by using the JsonResult class.
---

**Contents**

[TOC]

# Section 1: Setting up the Page

In order to return a JSON object from an ASP.NET page, the page must be set up to accept and process JSON requests. This can be done by adding the following code to the page:

```
<%@ Page Language="C#" AutoEventWireup="true" CodeFile="MyPage.aspx.cs" Inherits="MyPage" %>
<%@ Import Namespace="System.Web.Script.Serialization" %>
```

# Section 2: Processing the Request

Next, the page must be set up to process the request. This can be done by adding the following code to the page:

```
protected void Page_Load(object sender, EventArgs e)
{
    if (Request.HttpMethod == "POST")
    {
        // Deserialize the JSON object
        JavaScriptSerializer serializer = new JavaScriptSerializer();
        MyObject obj = serializer.Deserialize<MyObject>(Request.Form[0]);
    }
}
```

# Section 3: Returning the Response

Finally, the page must be set up to return the response. This can be done by adding the following code to the page:

```
protected void Page_Load(object sender, EventArgs e)
{
    if (Request.HttpMethod == "POST")
    {
        // Deserialize the JSON object
        JavaScriptSerializer serializer = new JavaScriptSerializer();
        MyObject obj = serializer.Deserialize<MyObject>(Request.Form[0]);
        
        // Serialize the response object
        string json = serializer.Serialize(obj);
        
        // Return the response
        Response.ContentType = "application/json";
        Response.Write(json);
        Response.End();
    }
}
```

# Section 4: Testing the Response

Once the page is set up to return the response, it can be tested by sending a request to the page with a JSON object. The response should be the same JSON object that was sent in the request.
