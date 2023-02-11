---
title: What is the process for creating a JSON log from nginx?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: Set the `log\_format` directive in nginx.conf to `json` to generate a JSON log from nginx.
---

**Contents**

[TOC]

# Section 1: Install jq

The first step to generate a JSON log from nginx in JSON is to install jq. jq is a lightweight and flexible command-line JSON processor. To install jq, you can use your package manager, such as apt-get or yum, or you can download and install it from the official jq website.

# Section 2: Configure nginx

The next step is to configure nginx to output its logs in JSON format. This can be done by adding a “log_format” directive to the nginx configuration file. This directive specifies the format of the log entries, and can be set to “json” to output the log entries in JSON format.

# Section 3: Restart nginx

Once the configuration has been updated, nginx needs to be restarted in order for the changes to take effect. This can be done by running the “nginx -s reload” command.

# Section 4: Generate JSON log

The final step is to generate a JSON log from nginx. This can be done by running the “tail -f /var/log/nginx/access.log | jq .” command. This will output the log entries in JSON format.
