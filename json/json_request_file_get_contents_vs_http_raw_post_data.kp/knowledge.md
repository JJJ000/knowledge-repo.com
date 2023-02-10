---
title: Which method is better for retrieving the body of a JSON request file_get_contents("php//input") or $http_raw_post_data?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: It is recommended to use file\_get\_contents(`php//input`) to get the body of a JSON request.
---

**Contents**

[TOC]

1. `php://input`
    - `php://input` is a read-only stream that allows you to read raw data from the request body.
    - It is a preferable way to get the body of JSON request as it is more direct and efficient than `$HTTP_RAW_POST_DATA`.
    - `php://input` is not available with enctype="multipart/form-data".

2. `$HTTP_RAW_POST_DATA`
    - `$HTTP_RAW_POST_DATA` is an option to access raw post data.
    - It can be used to get the body of JSON request, however, it is not as efficient as `php://input` as it does not have support for HTTP method PUT or DELETE. 
    - `$HTTP_RAW_POST_DATA` is available with enctype="multipart/form-data".
