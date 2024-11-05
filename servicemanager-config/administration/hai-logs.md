---
title: Hornbill AI Logs
description: This guide covers the functionality of the HAi Logs, Discover how to filter logs by User, Product Area, and Prompt to track the last 30 days' usage.
coverImage: /_books/servicemanager-config/administration/images/hai-cover.jpg
layout: article-toc
---

# HAi Logs

## Logs Access

The HAi Logs are available to any user associated with one of the following roles: 

|Role|Description|
|-|-|
|Service Desk Admin|This role is for a Service Desk Administrator. This includes, an elevated visibility to Requests and associated actions, the ability to configure Service Manager features via the Administration Tool and the option to restart a failed BPM within a Request.|

Additionally, any user with the application right **rightA.administerServiceDesk** can enable HAi features.

## Overview

The HAi Usage Logs show the last 30 days' usage with the latest first limited to 1000 rows. These logs can be filtered by User, Product Area, and Prompt. The Tokens Input/Output are an indication of the volume of input and text generated as an output when using prompts - and are the values that supply the dashboard with savings. Accepted is whether the output was accepted after generation or not. The Detailed Log allows you to view the unformatted input and output and is very useful for debugging output formatting errors.
![Hornbill AI Logs](/_books/servicemanager-config/administration/images/hai-logs.png)

## Retention

Currently all log history is kept, the UI restricts logs to the last 30 days and in the future the input and output text will be pruned after 30 days leaving only the details of the request. 

## Monitoring of Logs

Unlike AI-Assist which does not log its usage, HAi Usage is logged so customers can demonstrate the value being added to their business and debug issues. Hornbill will from time to time use these logs for both usage monitoring as well as improve the quality of the prompts output and to improve the overall service. Customer data confidentiality is maintained and any logs viewed by the Hornbill AI Team are anonymized before being removed from the customer Instance. Details can be found in section 6 of the [Hornbill Subscription agreement](https://www.hornbill.com/subscription-agreements).