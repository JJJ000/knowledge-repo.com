---
title: Obtain a file using an Android device, displaying the progress in a progressdialog
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use an AsyncTask to download the file in the background, and update the ProgressDialog with the progress of the download.
---

**Contents**

[TOC]

### Using AsyncTask

The following code uses an AsyncTask to download a file, and shows the progress in a ProgressDialog.

```java
public class DownloadFile extends AsyncTask<String, Integer, String> {
    ProgressDialog progressDialog;
    @Override
    protected void onPreExecute() {
        progressDialog = new ProgressDialog(context);
        progressDialog.setMessage("Downloading...");
        progressDialog.setIndeterminate(false);
        progressDialog.setMax(100);
        progressDialog.setProgressStyle(ProgressDialog.STYLE_HORIZONTAL);
        progressDialog.setCancelable(true);
        progressDialog.show();
    }

    @Override
    protected String doInBackground(String... params) {
        int count;
        try {
            URL url = new URL(params[0]);
            URLConnection connection = url.openConnection();
            connection.connect();
            // this will be useful so that you can show a typical 0-100% progress bar
            int lengthOfFile = connection.getContentLength();
            // download the file
            InputStream input = new BufferedInputStream(url.openStream(), 8192);
            // Output stream
            OutputStream output = new FileOutputStream("/sdcard/file_name.extension");

            byte data[] = new byte[1024];
            long total = 0;
            while ((count = input.read(data)) != -1) {
                total += count;
                // publishing the progress....
                publishProgress((int) (total * 100 / lengthOfFile));
                output.write(data, 0, count);
            }
            output.flush();
            output.close();
            input.close();
        } catch (Exception e) {
        }
        return null;
    }

    @Override
    protected void onProgressUpdate(Integer... values) {
        progressDialog.setProgress(values[0]);
    }

    @Override
    protected void onPostExecute(String s) {
        progressDialog.dismiss();
    }
}
```

### Using DownloadManager

The following code uses the DownloadManager class to download a file, and shows the progress in a ProgressDialog.

```java
public class DownloadFileWithDownloadManager extends AsyncTask<String, Integer, String> {
    ProgressDialog progressDialog;
    DownloadManager downloadManager;
    long downloadReference;

    @Override
    protected void onPreExecute() {
        progressDialog = new ProgressDialog(context);
        progressDialog.setMessage("Downloading...");
        progressDialog.setIndeterminate(false);
        progressDialog.setMax(100);
        progressDialog.setProgressStyle(ProgressDialog.STYLE_HORIZONTAL);
        progressDialog.setCancelable(true);
        progressDialog.show();
    }

    @Override
    protected String doInBackground(String... params) {
        downloadManager = (DownloadManager)context.getSystemService(Context.DOWNLOAD_SERVICE);
        Uri Download_Uri = Uri.parse(params[0]);
        DownloadManager.Request request = new DownloadManager.Request(Download_Uri);

        //Restrict the types of networks over which this download may proceed.
        request.setAllowedNetworkTypes(DownloadManager.Request.NETWORK_WIFI | DownloadManager.Request.NETWORK_MOBILE);
        //Set whether this download may proceed over a roaming connection.
        request.setAllowedOverRoaming(false);
        //Set the title of this download, to be displayed in notifications (if enabled).
        request.setTitle("Downloading");
        //Set a description of this download, to be displayed in notifications (if enabled)
        request.setDescription("Downloading file...");
        //Set the local destination for the downloaded file to a path within the application's external files directory
        request.setDestinationInExternalFilesDir(context, Environment.DIRECTORY_DOWNLOADS, "file_name.extension");

        downloadReference = downloadManager.enqueue(request);
        return null;
    }

    @Override
    protected void onProgressUpdate(Integer... values) {
        DownloadManager.Query q = new DownloadManager.Query();
        q.setFilterById(downloadReference);
        Cursor cursor = downloadManager.query(q);
        cursor.moveToFirst();
        int bytes_downloaded = cursor.get
