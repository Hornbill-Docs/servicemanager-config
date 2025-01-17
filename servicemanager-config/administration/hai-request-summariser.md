---
title: Hornbill AI Request Summariser 
description: This guide covers the configuration of Request Summariser for HAi (Hornbill AI) within your environment. .
coverImage: /_books/servicemanager-config/administration/images/hai-cover.jpg
layout: article-toc
---

# Configure HAi - Request Summariser

::: important
HAi is currently in a closed beta, speak to customer success should you want to take part.
:::

## Setup

Once [enabled](/servicemanager-config/administration/hai#enabling-hai-features) there are some settings explained in the table below that allow for some customization on the amount of date and what timeline update types are used when generating the request summary, these can be updated by access [application settings](/servicemanager-config/advanced-tools-and-settings/application-settings) for service manager.

|Setting|Description|
|-|-|
|generativeAi.requestSummary.availablePostTypes|List of timeline update types sent to the summariser, this allows you to add in or remove certain update types to be included or excluded from the request summary by default this is set to  ```Authorization,Customer,Email,Escalate,update```|
|generativeAi.requestSummary.format| Format the request summary is generated in (Structured or Conversational) |
|generativeAi.requestSummaryAutoUpdates|Auto generate Request Summary when a request is opened|
|generativeAi.limits.activitySteamPosts|Limit on the number of posts returned and passed to the summariser, by default this is set to ```100``` ordered by most recent activity|
|generativeAi.limits.activitySteamComments|Limit on the number of comments per post returned and passed to the summariser, by default this is set to  ```100```|
|generativeAi.limits.activitySteamContentLength|Limit on the maximum content length of a post or comment, anything longer is truncated and passed to the summariser, by default this is set to  ```1000```|

## Limits

The reason for the limits is to minimize the likely hood of a request summary request to our AI Services reaching the total number of input tokens allowed, currently 128,000. Very long timelines with lots of large posts can go over this limit. Internally there is a safe guard that even if you crank the limits up a very large timeline will still end up truncated in an effort to prevent the AI Service returning an error. The maximum input tokens has been slowly increasing over the months and some services allow for much much larger inputs, something that may be investigated should the limits prove problematic for customers.