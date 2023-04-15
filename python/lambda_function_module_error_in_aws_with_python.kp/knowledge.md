---
title: Python encountered an aws error stating that the module named "lambda_function" was not found
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The lambda function name in AWS does not match the name of the corresponding Python file or module.
---

**Contents**

[TOC]

# Introduction
AWS (Amazon Web Services) is a cloud computing platform that provides various services such as computing power, storage, and databases. It allows users to deploy and manage applications and services at a lower cost compared to traditional on-premise solutions. AWS Lambda is a serverless computing service provided by AWS, which allows developers to run their code without having to manage servers.

# Error: No module named lambda_function
If you encounter the error message "No module named lambda_function" in Python while running an AWS Lambda function, it means that there is a problem with the Lambda function's name or structure. The lambda_function is a default name given to the function that is executed by AWS Lambda when it is triggered. If the name is changed, the AWS Lambda service may not be able to find it, resulting in the above error message.

# Solution
To fix the "No module named lambda_function" error message in AWS Lambda, you must ensure that the name of the function is correct and has no typos or misspellings. 

1. Check the file name and function name in the AWS Lambda console. Make sure the name matches the code you have written.

2. Ensure that the file is saved with the correct extension (usually .py for Python code).

3. Ensure that the function is written correctly and has no syntax errors or typos.

4. Finally, test the function again and check for any other errors that may occur.

# Conclusion
In summary, the "No module named lambda_function" error message in AWS Lambda is a common error that occurs when the function name or structure is incorrect. By following the above solution, you can quickly fix the error and get your function up and running again.
