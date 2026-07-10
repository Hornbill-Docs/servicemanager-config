---
layout: article-toc
---

# Configure HAi - Email Attachment Labeling

::: important
HAi is currently in a closed beta, speak to customer success should you want to take part.
:::

## Setup

Once [enabled](/servicemanager-config/administration/hai) there are some settings explained in the table below that allow for some customization on the amount of date and what timeline update types are used when generating the request summary, these can be updated by access [application settings](/servicemanager-config/advanced-tools-and-settings/application-settings) for service manager.

|Setting|Description|
|-|-|
|generativeAi.emailAttachmentLabeling.typesToSelect|List of image types that will be kept selected when processing an email for associating or logging against a request ```Government ID,Screenshot,Photo,Scanned Document,Document,Image``` ```Company Logo``` and ```Icon``` are disabled by default|
|generativeAi.emailAttachmentLabelingAutoUpdates|Auto Email Attachment Labeling when an email is processed against a request as an update and Auto Responder|
