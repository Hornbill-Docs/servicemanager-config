---
title: Integration via webhooks
layout: article
---
# Integration via webhooks
This article discusses things to consider if you plan to use webhooks in Hornbill for integration.

## Topics covered
* [Before you begin](/servicemanager-config/administration/integration-webhooks#before-you-begin)
* [Custom fields in Service Manager](/servicemanager-config/administration/integration-webhooks#custom-fields-in-service-manager)
* [Triggering webhooks in Hornbill](/servicemanager-config/administration/integration-webhooks#triggering-webhooks-in-hornbill)

## Before you begin
* Read about using webhooks in Hornbill in [Hornbill Platform Fundamentals](/esp-fundamentals/core-capabilities/integration/web-hooks).
* You can create webhooks in **Configuration** > **Platform Configuration** > **Integration** > **Webhooks**. See the [Hornbill Platform Configuration Guide](/esp-config/integration/webhooks) for details.

## Custom fields in Service Manager
If you plan to use webhook services in your Hornbill implementation, then it is important to consider how you use your custom fields.

If you want to use custom field values in the webhooks, you should reserve the first 30 custom fields for those values that need to be expressed for webhook triggers. While in Service Manager there are 80 custom fields, the webhook options in the trigger expression only go up to Custom 30.

## Triggering webhooks in Hornbill
In Hornbill, webhooks function on entities. Because webhooks are entity-bound, you cannot trigger a webhook for one entity on an event in another entity. Consider this when making use of the custom fields available for webhooks, and when creating your trigger expressions.