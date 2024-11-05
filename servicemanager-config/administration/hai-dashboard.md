---
title: Hornbill AI Dashboard
description: Discover how to maximize the potential of the HAi Dashboard in your organization with roles tailored to your needs. Get insights on usage statistics, estimated hours saved through generative AI, and track your organization's performance over time. Learn about the key features and application settings that drive the value dashboard, providing valuable metrics for decision-making and efficiency improvements.
coverImage: /_books/servicemanager-config/administration/images/hai-cover.jpg
layout: article-toc
---

# HAi Dashboard

## Dashboard Access

The HAi Dashboard is available to any user associated with one of the following roles: 

|Role|Description|
|-|-|
|Service Desk Admin|This role is for a Service Desk Administrator. This includes, an elevated visibility to Requests and associated actions, the ability to configure Service Manager features via the Administration Tool and the option to restart a failed BPM within a Request.|

Additionally, any user with the application right **rightA.administerServiceDesk** can enable HAi features.

## Overview

The HAi Value Dashboard is designed to show you your organization's usage of HAi and estimate hours saved through generative AI (summarizing as generating text output). These calculations are estimates and are configurable. The top-line widgets show rolling 30-day usage and savings.

The first two line charts show the savings per month over the last 12 months. This will take a few weeks of usage before output is properly populated.

The second two charts show (1) Usage per day for the last 30 days by product area and (2) The top 4 most active users based on prompt usage over the last 30 days.
Currently, no additional filters can be applied to the dashboard.
![Hornbill AI Dashboard](/_books/servicemanager-config/administration/images/hai-dashboard.png)

## Configuration

The following application settings control the calculations on the value dashboard

|Setting|Description|Default|
|-|-|-|
|generativeAi.dashboard.currencySymbol|Currency to use when displaying value saved based on ratePerMinute.|£|
|generativeAi.dashboard.ratePerMinute|Lowest FTE cost per minute based on currency from currencySymbol.|0.2|
|generativeAi.dashboard.readingRate|Average words per minute reading a document.|200|
|generativeAi.dashboard.typeingRate|Average words per minute when typing a document.|40|
|generativeAi.dashboard.wordsPerToken|Estimate the number of words per token to convert tokens from prompts to words.|1.3|
