---
description: Discover how to maximize the potential of the HAi Dashboard in your organization with roles tailored to your needs. Get insights on usage statistics, estimated hours saved through generative AI, and track your organization's performance over time. Learn about the key features and application settings that drive the value dashboard, providing valuable metrics for decision-making and efficiency improvements.
coverImage: /_books/servicemanager-config/administration/images/hai-cover.jpg
layout: article-toc
---

# HAi Dashboard

## Dashboard Access

The HAi Dashboard is available to any user associated with one of the following roles:

|Role|Application|Description|
|-|-|-|
|Service Desk Admin|Service Manager|This role is for a Service Desk Administrator. This includes elevated visibility of Requests and associated actions, the ability to configure Service Manager features via the Administration Tool, and the option to restart a failed BPM within a Request.|
|HAi Manager|Platform|This role should only be used for managing HAi configurations.|

Additionally, any user with the application right **rightA.administerServiceDesk** can enable HAi features.

## Overview

The HAi Value Dashboard is designed to show you your organization's usage of HAi and estimate hours saved through using AI. These calculations are estimates and are configurable. The top-line widgets show rolling 30-day usage and savings.

A dashboard option allows you to select between agent efficiency and deflection.

* **Agent Efficiency**: The time saved by your agents using generative HAi features that shift routine tasks from humans, reducing manual workloads and routine touchpoints.
* **Agent Deflection**: The reduction of inbound service desk requests by diverting routine user requests to conversational virtual assistants and intelligent self-service.

### Agent Efficiency charts

The first two line charts show the savings per month over the last 12 months. It will take a few weeks of usage before these charts are properly populated.

The next two charts show (1) usage per day by product area over the last 30 days and (2) the top four most active users based on prompt usage over the last 30 days.

![Hornbill AI Dashboard](/_books/servicemanager-config/administration/images/hai-dashboard.png)

### Agent Deflection charts

Hornbill Agent Deflection is a capability that shifts routine support interactions away from human service desk agents to AI-powered virtual agents and automated self-service channels.

![Agent Deflection Dashboard](/_books/servicemanager-config/administration/images/hai-agent-deflection-dashboard.png)

#### What is counted

Only conversations between end users and the HAi User Assistant are counted. Chats where an Analyst is using the HAi Analyst Assistant are excluded.

| Measure | What it means |
| --- | --- |
| Chats | The number of different conversations in which the end user sent at least one message. |
| Solved | The number of chats the end user marked as solved. Marking a chat as solved makes it read only, so the conversation can no longer be continued. |
| Deflections | Solved chats where the agent resolved the issue without performing an action on the user's behalf (raise request) and without handing the user over to a human. Every deflection is a solved chat, but not every solved chat is a deflection. |
| Time | The average time taken to solve a chat, in minutes. It is measured from when the chat was created to when the end user marked it as solved, and rounded up to the next whole minute. |

#### Available charts

* **HAi User Assistant Overview**: This chart shows the total number of chats, the number of resolved issues, and how many of these were deflected from a real agent. It will take a few weeks of usage before this chart is properly populated.
* **Average Chat Duration**: This chart shows the average duration of chats over the last 12 months.
* **Deflection Rate**: This chart shows the percentage of the chats that were deflected from a real agent over the last 12 months.

## Configuration

The following application settings control the calculations on the value dashboard:

|Setting|Description|Default|
|-|-|-|
|generativeAi.dashboard.currencySymbol|Currency symbol to use when displaying the value saved, based on ratePerMinute.|£|
|generativeAi.dashboard.ratePerMinute|Lowest FTE cost per minute, in the currency set by currencySymbol.|0.2|
|generativeAi.dashboard.readingRate|Average characters per minute reading a document.|800|
|generativeAi.dashboard.typingRate|Average characters per minute when typing a document.|150|
