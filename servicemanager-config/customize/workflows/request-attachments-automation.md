---
layout: article-toc
---
# Request Attachments Automation

Use the Request Attachments automation to manage attachments that are linked to a request.

![Request Attachments automation](/_books/servicemanager-config/customize/workflows/images/request-attachments-automation.png)

## Request attachment tasks

### Remove Attachments

This task will remove attachments from the request using the specified options.

* This automation can be used to remove known image files that have been added to a request when the request has been raised by an email that includes images in an email signature.
* For security, some attachments may need to be removed once they have been processed and there is no further need to keep them.
* To help maintain space utilization, after a request has been closed, attachments can be removed.  Using the **Exclusion** option, you can specify the attachments that you want to keep.

#### Options

* **Request ID**: This is a mandatory field.  Setting this to **Auto** will use the global variable for the request that the workflow is running on.
* **Included File Extensions**: Add one or more file extensions that match the files that need to be removed.
* **Include Key Words**: Comma-separated list of keywords. Attachment filenames that include a key word are to be removed.
* **Exclude Key Words**: Comma-separated list of keywords. Attachment filenames that include a key word are not to be removed.
