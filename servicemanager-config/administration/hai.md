---
title: Hornbill AI Configuration
description: This guide covers the configuration and implementation of HAi (Hornbill AI) features within your environment. The document outlines step-by-step instructions on enabling HAi capabilities for your user account, specifying the necessary roles, and accessing the necessary settings in Hornbill.
coverImage: /_books/servicemanager-config/administration/images/hai-cover.jpg
layout: article-toc
---

# Configure HAi

::: important
HAi is currently in a closed beta, speak to customer success should you want to take part.
:::

## Enabling HAi features

Your instance needs a [HAi Service](/esp-fundamentals/core-capabilities/integration/hai-services) set before enabling any of the HAi Features in Service Manager.

All HAi features within Service Manager are *disabled* by default and must be individually enabled before they can be used by end users. To enable any of the HAi capabilities in Service Manager, your User Account must be associated with the following roles:

|Role|Application|Description|
|-|-|-|
|Service Desk Admin|Service Manager|This role is for a Service Desk Administrator. This includes, an elevated visibility to Requests and associated actions, the ability to configure Service Manager features via the Administration Tool and the option to restart a failed BPM within a Request.|
|HAi User|Service Manager|This role allows users to access HAi functionality inside of Service Manager|
|HAi Manager|Platform|This role should only be used for managing HAi configurations.|

## How to enable HAi features

* Log into Hornbill with the relevant access role.
* Click on the settings gear icon in the lower left of the screen.
* Change the dropdown from '''My Personal Settings''' to '''Service Manager'''.
* Click on HAi under Administration in the left-hand menu.
* Enable the required feature(s).

![Hornbill AI Configuration](/_books/servicemanager-config/administration/images/hai-config.png)

## Grant Users Access to HAi features

To access the HAi capabilities of Hornbill Service Manager, your User Account must have one of the following Service Manager roles associated.

|Role|Description|
|-|-|
|HAi User|This role allows users to access HAi functionality inside of Service Manager|

## Data

### HAi Providers

By enabling any of these optional HAi features, you are agreeing to allow a third party to process your data ([HAi Providers](/servicemanager-config/administration/hai-providers)), Data from prompts and underlying request data is passed to a Provider using encrypted connections see [HAi Providers](/servicemanager-config/administration/hai-providers) for further details.

The following areas of functionality send request data during each invocation and are document as follows:

### Request Summariser

When summarizing a request the following data from the request you are in is processed:

```JSON

    h_itsm_requests.h_description
    h_itsm_requests.h_summary
    h_itsm_requests.h_fk_user_name

```

The timeline of the request is filtered down with the following filters '["Authorization","Customer","Email","Escalate","update"]' and can be updated [here](/servicemanager-config/administration/hai-request-summariser)

Each post in the timelines sends the following

```JSON

    actorInfo.name
    content

```

Each comment associated to any filtered posts in the timelines sends the following

```JSON

    actorInfo.name
    comment

```

Custom Questions (first 100) are passed, excluding the type `file-upload` and `label` and are paired with the question text as follows:

```JSON

    h_question
    h_answer_value

```

Completed Tasks information as follows:

```JSON

    title
    category
    owner
    outcome
    completedon
    details
    assigned
    reference

```

### Suggest Resolution

When suggesting a resolution against a request the following data from the request you are in is processed:

```JSON

    h_itsm_requests.h_description
    h_itsm_requests.h_summary
    h_itsm_requests.h_fk_user_name

```

The timeline of the request is filtered down with the following filters '["Update","Email",'Customer']'

Each post in the timelines sends the following

```JSON

    actorInfo.name
    content

```

Each comment associated to any filtered posts in the timelines sends the following

```JSON

    actorInfo.name
    comment

```

### Knowledge Draft

When generating a knowledge draft from a resolved or closed request the following data is sent:

```JSON

    h_itsm_requests.h_description
    h_itsm_requests.h_summary
    h_itsm_requests.h_resolution

```

### Text Assist

Text assist combined with snippets or used withing a workflow and passing in variables can pass any data a user has selected to pass to a [HAi Provider](/servicemanager-config/administration/hai-providers), nothing is sent automatically. In the case of snippets, when the snippet is selected the analyst will see the data before the text is passed as part of the prompt when using Text Assist after a snippet.

### Sentiment Analysis

When using sentiment analysis for a request the following data from the request you are in is processed:

```JSON

    h_itsm_requests.h_description
    h_itsm_requests.h_summary
    h_itsm_requests.h_fk_user_name

```

The timeline of the request is filtered down with the following filters '["Customer","Email","update"]'

Each post in the timelines sends the following

```JSON

    actorInfo.name
    content

```

Each comment associated to any filtered posts in the timelines sends the following

```JSON

    actorInfo.name
    comment

```

Custom Questions (first 100) are passed, excluding the type `file-upload` and `label` and are paired with the question text as follows:

```JSON

    h_question
    h_answer_value

```
