---
title: Hornbill AI Sentiment Analysis
description: This guide covers the configuration of Sentiment Analysis for HAi (Hornbill Ai) within your environment. .
coverImage: /_books/servicemanager-config/administration/images/hai-cover.jpg
layout: article-toc
---
# Configure HAi - Sentiment Analysis
::: important 
HAi is currently in a closed beta, speak to customer success should you want to take part.
::: 

## Auto Updates

Once [enabled](/servicemanager-config/administration/hai#enabling-hai-features) there is an additional check box for Sentiment Analysis called ```Auto Updates``` once enabled all requests will have their sentiment checked when the following criteria are met:
* Customer Portal Timeline Post or Comment - If the person posting or commenting is the customer of the request
* Employee Portal Timeline Post or Comment - If the person posting or commenting is the customer of the request
* Email Auto Responder updates a request - If the person sending the email is the customer of the request
* Email Applied to a request from a mailbox - If the person sending the email is the customer of the request