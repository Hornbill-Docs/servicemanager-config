---
title: Hornbill AI Providers
description: This guide covers the third party Providers for HAi (Hornbill AI) within your environment.
coverImage: /_books/servicemanager-config/administration/images/hai-cover.jpg
layout: article-toc
---

# HAi Providers

Hornbill AI utilizes the latest advancements in generative AI from world class providers, by default this provider is **OpenAI**; making use of the latest models available to use Hornbill AI out of the box prompts are tailed to provide the best experience possible. OpenAI data processing is not locked to a specific region nor do they currently provide API integrations like ours any control of which region the prompts are processed in, for this reason a second generative AI provider was added **Azure OpenAI Service**. When enabling Generative AI on your Hornbill Instance you will be able to select one of two providers you governance teams are happy to engage with

## HAi Provider Details

Changing the HAi Provider can be done by selecting a [HAi Service](/esp-fundamentals/core-capabilities/integration/hai-services) as part of the Platform Configuration, anyone with ```sys.c.manageIntegrations``` system right can set or change a provider.

## OpenAI

Data from prompts and underlying request data is passed to OpenAI under their [business terms](https://openai.com/policies/business-terms) of use and their [enterprise privacy policy](https://openai.com/enterprise-privacy). This prevents usage data from being used for training new models, the input and output of prompts is currently stored by OpenAI as outlined in their [documentation](https://platform.openai.com/docs/models/how-we-use-your-data), all data is sent using encrypted connection.

### Data Processing (OpenAI)

OpenAIs [Data Processing Addendum covers](https://openai.com/policies/data-processing-addendum/) any specifics they have documented on any possible international transfer of data.

### Usage (OpenAI)

Usage of the OpenAI API's goes through an API Key provided by hornbill. Currently there are no usage limits outside the limits provided by OpenAI.

## Azure AI Service

**Azure OpenAI Service** is an Azure service provided by Microsoft that hosts OpenAI Models in Azure regions for use by Microsoft customers, unlike dealing with OpenAI directly this allows an API integration with an OpenAI model to have guarantees on where data is being processed. The underlying models are the same so the functionality provided by the API integration back to the end user is the same.

### Data Processing (Azure)

Data from prompts and underlying request data is passed to Azure for processing in a specific region, this region will be listed against the [provider name when selected](/esp-fundamentals/core-capabilities/integration/hai-services), details on how Azure processing this data can be found [here](https://learn.microsoft.com/en-us/legal/cognitive-services/openai/data-privacy).

As with OpenAI, **Azure OpenAI Services** has a built in abuse monitoring that logs input and output prompts, these are stored in the same region and kept for 30 days, details can be found in their [data privacy details](https://learn.microsoft.com/en-us/legal/cognitive-services/openai/data-privacy).

### Usage (Azure)

Usage of the **Azure OpenAI Services** API's is provided through deployments managed by Hornbill. Currently there are no usage limits outside the limits provided by Azure, It is possible for a customer to provider their own **Azure OpenAI Services** deployment details instead of using the deployment provided by Hornbill.

## Provider terms of use

Details on each providers usage policy as well as Hornbill's can be found [here](/servicemanager-config/administration/hai-usage-policy)