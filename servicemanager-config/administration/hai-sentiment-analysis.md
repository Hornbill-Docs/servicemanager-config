---
title: Hornbill AI Sentiment Analysis
description: This guide covers the configuration of Sentiment Analysis for HAi (Hornbill AI) within your environment. .
coverImage: /_books/servicemanager-config/administration/images/hai-cover.jpg
layout: article-toc
---

# Configure HAi - Sentiment Analysis

::: important
HAi is currently in a closed beta, speak to customer success should you want to take part.
:::

## Setup

Once [enabled](/servicemanager-config/administration/hai#enabling-hai-features) there are some settings explained in the table below that allow for some customization on the amount of date and what timeline update types are used when generating the request summary, these can be updated by access [application settings](/servicemanager-config/advanced-tools-and-settings/application-settings) for service manager.

|Setting|Description|
|-|-|
|generativeAi.sentimentAnalysis.availablePostTypes|This setting determines the type of posts that are used to generate the request sentiment ```Authorization,Customer,Email,Escalate,update```|
|generativeAi.sentimentAnalysisAutoUpdates|Auto Request Sentiment Analysis on Customer Updates|

## Auto Updates

```Auto Updates``` when enabled will trigger any request to have their sentiment checked when the following criteria are met:

* Customer Portal Timeline Post or Comment - If the person posting or commenting is the customer of the request
* Employee Portal Timeline Post or Comment - If the person posting or commenting is the customer of the request
* Email Auto Responder updates a request - If the person sending the email is the customer of the request
* Email Applied to a request from a mailbox - If the person sending the email is the customer of the request
