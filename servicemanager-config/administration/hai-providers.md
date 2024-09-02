---
title: Hornbill AI Providers
description: This guide covers the third party Providers for HAi (Hornbill AI) within your environment.
coverImage: /_books/servicemanager-config/administration/images/hai-cover.jpg
layout: article-toc
---
# HAi Providers

Hornbill AI utilizes the latest advancements in generative AI from world class providers, by default this provider is **OpenAI**; making use of the latest models available to use Hornbill AI out of the box prompts are tailed to provide the best experience possible. OpenAI data processing is not locked to a specific region nor do they currently provide API integrations like ours any control of which region the prompts are processed in, for this reason a second generative AI provider was added **Azure Open AI Service**. When signing up for Hornbill AI you will be asked which of the two providers you governance teams are happy to engage with and if **Azure Open AI Service** is selected generative AI processing will be limited to the region your Hornbill Instance is hosted in, so a UK Customer will have all generative AI processing performed in the UK utilizing a Microsoft Azure region for the UK.

It is possible to change providers after the initial selection and reaching out to your customer success contact is the best point of call for this, the ability for a customer to change this is currently limited to prevent accidental change by an administrator that goes against the agreement of a customers governance and compliance teams. 

## HAi Provider Details
Currently their is no UI for showing which HAI Provider your instance is configured with, reach out to customer success if in doubt and the current setup can be clarified. 


## OpenAI
Data from prompts and underlying request data is passed to OpenAI under their [business terms](https://openai.com/policies/business-terms) of use and their [enterprise privacy policy](https://openai.com/enterprise-privacy). This prevents usage data from being used for training new models, the input and output of prompts is currently stored by OpenAI as outlined in their [Documentation](https://platform.openai.com/docs/models/how-we-use-your-data), all data is sent using encrypted connection.

### Data Processing
OpenAIs [Data Processing Addendum covers](https://openai.com/policies/data-processing-addendum/) any specifics they have documented on any possible international transfer of data.

### Usage
Usage of the OpenAI API's goes through an API Key provided by hornbill. Currently there are no usage limits outside the limits provided by OpenAI. It is possible to override the API to use an API Key of your organization's choice by overriding the system setting **integration.hai.openai.apiKey**.

Further details on this here: https://docs.hornbill.com/esp-fundamentals/productivity/ai-assist


## Azure AI Service
**Azure OpenAI Services** is an Azure services provided by microsoft that hosts OpenAI Models in Azure regions for use by Microsoft customers, unlike dealing with OpenAI directly this allows a API integration with a OpenAI model to have guarantees on where data is being processed. The underlying models are the same so the functionality provided by the API integration back to the end user is the same (model availability depending).

### Data Processing
Data from prompts and underlying request data is passed to Azure for processing in a specific region, unless otherwise requested this region will be the same geographic region that your Hornbill Instance is hosted on, details on how Azure processing this data can be found [here](https://learn.microsoft.com/en-us/legal/cognitive-services/openai/data-privacy).

As with OpenAI, **Azure OpenAI Services** has a built in abuse monitor that logs input and output prompts, these are stored in the same region and kept for 30 days, details can be found in their [data privacy details](https://learn.microsoft.com/en-us/legal/cognitive-services/openai/data-privacy).

### Usage
Usage of the **Azure OpenAI Services** API's is provided through deployments managed by Hornbill. Currently there are no usage limits outside the limits provided by Azure, It is possible for a customer to provider their own **Azure OpenAI Services** deployment details instead of using the deployment provided by Hornbill, reach out to you customer success contact to discuss this. 


## Provider terms of use
Details on each providers usage policy as well as Hornbill's can be found [here](/servicemanager-config/administration/hai-usage-policy)