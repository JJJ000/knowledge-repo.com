---
title: What is the procedure to incorporate a custom ca root certificate into the ca store employed by pip in windows?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Add the root certificate to the cacert.pem file located in the \Lib\site-packages\certifi folder within your Python installation directory.
---

**Contents**

[TOC]

# Overview 

When using `pip` to install packages in Python, it relies on the installed SSL root certificates for secure communication. However, sometimes there may be a need to add custom root CA certificates. 

In this guide, we will go through the process of adding a custom root CA certificate to the CA store used by `pip` in Windows for Python. This process involves 4 main steps: 

1. Identify the location of the CA store used by `pip` 
2. Generate a custom root CA certificate 
3. Add the custom root CA certificate to the CA store 
4. Verify that the custom root CA certificate has been added correctly 

# Step 1 – Identify the location of the CA store 

Before we can add a custom root CA certificate to the CA store, we need to know where the CA store is located. 

In Windows, `pip` uses the `certifi` package as its trusted certificate authority. This means that we need to find the location of the `certifi` package in our Python installation. 

To do this, open a command prompt and run the following command: 

```
python -c "import certifi; print(certifi.where())"
```

This will output the file path of the `cacert.pem` file, which represents the CA store used by `pip`. 

# Step 2 – Generate a custom root CA certificate 

There are various ways to generate a custom root CA certificate, but we will use the `openssl` utility for this guide. 

First, download and install OpenSSL from [https://www.openssl.org/](https://www.openssl.org/) if it is not already installed. 

Open a command prompt and navigate to a directory where you want to store the custom root CA certificate. Then, run the following command to generate a private key: 

```
openssl genrsa -des3 -out custom_ca.key 2048
```

This will generate a private key file named `custom_ca.key`. Keep this file secure, as it will be used to sign and verify the custom root CA certificate. 

Next, run the following command to generate a CSR (Certificate Signing Request): 

```
openssl req -new -key custom_ca.key -out custom_ca.csr
```

This will generate a CSR file named `custom_ca.csr`. Fill in the required details, such as the common name (CN), organization name, and country, when prompted. 

Finally, run the following command to generate the custom root CA certificate: 

```
openssl x509 -req -days 365 -in custom_ca.csr -signkey custom_ca.key -out custom_ca.crt
```

This will generate a custom root CA certificate named `custom_ca.crt`. 

# Step 3 – Add the custom root CA certificate to the CA store 

Now that we have generated a custom root CA certificate, we need to add it to the CA store used by `pip` in Windows. 

To do this, open the `cacert.pem` file in a text editor. Then, copy the contents of the `custom_ca.crt` file and paste it at the end of the `cacert.pem` file. Save the `cacert.pem` file. 

# Step 4 – Verify that the custom root CA certificate has been added correctly 

To verify that the custom root CA certificate has been added correctly to the CA store used by `pip` in Windows, open a command prompt and run the following command: 

```
python -c "import ssl; print(ssl.get_default_verify_paths())"
```

This will output the file paths of the certificate authority files used by `pip` in Windows. Check that the `cacert.pem` file that we modified in step 3 is listed. 

Alternatively, you can run the following command to verify that `pip` can use the custom root CA certificate: 

```
pip install --trusted-host pypi.org --trusted-host files.pythonhosted.org <package-name>
```

Replace `<package-name>` with the name of a package that you want to install from the Python Package Index (PyPI). If `pip` can install the package without any errors, then it means that the custom root CA certificate has been added correctly.
