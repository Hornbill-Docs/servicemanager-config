---
title: Hornbill AI Configuration
description: This guide covers the configuration and implementation of HAi (Hornbill Ai) features within your environment. The document outlines step-by-step instructions on enabling HAi capabilities for your user account, specifying the necessary roles, and accessing the necessary settings in Hornbill.
coverImage: /_books/servicemanager-config/administration/images/hai-cover.jpg
layout: article-toc
---
# Configure HAi
::: important 
HAi is currently in a closed beta, speak to customer success should you want to take part.
::: 
## Enabling HAi features
All HAi features are *disabled* by default and must be individually enabled before they can be used by end users. To enable any of the HAi capabilities, your User Account must be associated with one of the following roles: 

|Role|Description|
|-|-|
|Service Desk Admin|This role is for a Service Desk Administrator. This includes, an elevated visibility to Requests and associated actions, the ability to configure Service Manager features via the Administration Tool and the option to restart a failed BPM within a Request.|

Additionally, any user with the application right **rightA.administerServiceDesk** can enable HAi features.


## How to enable HAi features
* Log into Hornbill with the relevant access role.
* Click on the settings gear icon in the lower left of the screen.
* Change the dropdown from '''My Personal Settings''' to '''Service Manager'''.
* Click on HAi under Administration in the left-hand menu.
* Enable the required feature(s).

<img src="/_books/servicemanager-config/administration/images/hai-config.png" alt="Hornbill Ai Configuration" ></img>

## Grant Users Access to HAi features
To access the HAi capability of Hornbill Service Manager, your User Account must have one of the following roles associated.

|Role|Description|
|-|-|
|HAi User|This role allows users to access HAi functionality inside of Service Manager|

## Data 
### OpenAI Processor
By enabling any of these optional HAi features, you are agreeing to allow a third party to process your data (OpenAI), Data from prompts and underlying request data is passed to OpenAI under their [business terms](https://openai.com/policies/business-terms) of use and their [enterprise privacy policy](https://openai.com/enterprise-privacy). This prevents usage data from being used for training new models, the input and output of prompts is currently stored by OpenAI as outlined in their [Documentation](https://platform.openai.com/docs/models/how-we-use-your-data), all data is sent using encrypted connection.

OpenAIs [Data Processing Adendum covers](https://openai.com/policies/data-processing-addendum/) any specifics they have documented on any possible international transfer of data.

The following areas of functionality send request data during each invocation and are document as follows:
### Request Summariser 
When summarizing a request the following data from the request you are in is processed:
```

    h_itsm_requests.h_description
    h_itsm_requests.h_summary
    h_itsm_requests.h_fk_user_name

```
The timeline of the request is filtered down with the following filters '["Authorization","Customer","Email","Escalate","Task","update"]' and can be updated [here](/servicemanager-config/administration/hai-request-summariser)

Each post in the timelines sends the following
```

    actorInfo.name
    content

```

Each comment associated to any filtered posts in the timelines sends the following
```

    actorInfo.name
    comment

```

Custom Questions (first 100) are passed, excluding the type `file-upload` and `label` and are paired with the question text as follows:
```

    h_question
    h_answer_value

```

### Suggest Resolution
When suggesting a resolution against a request the following data from the request you are in is processed:
```

    h_itsm_requests.h_description
    h_itsm_requests.h_summary
    h_itsm_requests.h_fk_user_name

```
The timeline of the request is filtered down with the following filters '["Update","Email",'Customer']' 

Each post in the timelines sends the following
```

    actorInfo.name
    content

```

Each comment associated to any filtered posts in the timelines sends the following
```

    actorInfo.name
    comment

```
### Knowledge Draft
When generating a knowledge draft from a resolved or closed request the following data is sent:

```

    h_itsm_requests.h_description
    h_itsm_requests.h_summary
    h_itsm_requests.h_resolution

```


### Text Assist
Text assist combined with snippets or used withing a workflow and passing in variables can pass any data a user has selected to pass to OpenAI, nothing is sent automatically. In the case of snippets, when the snippet is selected the analyst will see the data before the text is passed as part of the prompt when using Text Assist after a snippet. 

### Sentiment Analysis
When using sentiment analysis for a request the following data from the request you are in is processed:
```

    h_itsm_requests.h_description
    h_itsm_requests.h_summary
    h_itsm_requests.h_fk_user_name

```
The timeline of the request is filtered down with the following filters '["Customer","Email","update"]'

Each post in the timelines sends the following
```

    actorInfo.name
    content

```

Each comment associated to any filtered posts in the timelines sends the following
```

    actorInfo.name
    comment

```

Custom Questions (first 100) are passed, excluding the type `file-upload` and `label` and are paired with the question text as follows:
```

    h_question
    h_answer_value

```


## OpenAI Usage
Usage of the OpenAI API's goes through an API Key provided by hornbill. Currently there are no usage limits outside the limits provided by OpenAI. It is possible to override the API to use an API Key of your organization's choice by overriding the system setting **integration.openai.apiKey**.

Further details on this here: https://docs.hornbill.com/esp-fundamentals/productivity/ai-assist