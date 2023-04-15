---
title: What is the process for downloading and saving a file from the internet using java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the URLConnection class to open a connection to the file, then use the InputStream and OutputStream classes to read and write the file to a local location.
---

**Contents**

[TOC]

### Downloading the File

Using the Java language, you can use the `java.net` package to download a file from the Internet. The following code snippet shows how to download a file from a URL and save it to a local file.

```java
// Create a URL object
URL url = new URL(urlString);

// Read the input stream
InputStream in = url.openStream();

// Create a file output stream
FileOutputStream fos = new FileOutputStream(filePath);

// Read bytes from the input stream and write to the output stream
byte[] buffer = new byte[1024];
int length;
while ((length = in.read(buffer)) > 0) {
    fos.write(buffer, 0, length);
}

// Close the streams
in.close();
fos.close();
```

### Saving the File

Once the file has been downloaded, you can save it to a local file. You can use the `java.io` package to save the file. The following code snippet shows how to save the file to a local file.

```java
// Create a file output stream
FileOutputStream fos = new FileOutputStream(filePath);

// Read bytes from the input stream and write to the output stream
byte[] buffer = new byte[1024];
int length;
while ((length = in.read(buffer)) > 0) {
    fos.write(buffer, 0, length);
}

// Close the stream
fos.close();
```

### Verifying the Download

Once the file has been downloaded and saved, you can verify the download by comparing the size of the file on the server with the size of the file on the local machine. You can use the `java.nio` package to compare the sizes. The following code snippet shows how to compare the sizes of the two files.

```java
// Get the size of the file on the server
URL url = new URL(urlString);
URLConnection conn = url.openConnection();
long serverFileSize = conn.getContentLengthLong();

// Get the size of the file on the local machine
Path localPath = Paths.get(filePath);
long localFileSize = Files.size(localPath);

// Compare the sizes
if (serverFileSize == localFileSize) {
    System.out.println("Download successful!");
} else {
    System.out.println("Download failed!");
}
```
