---
title: Create and manage partitions
layout: article
keywords: 
---
# Overview

::: note
This article is new, to support the preview release of the new Asset Management and its new UI.
:::

Asset management in Hornbill provides the ability to facilitate MSP or multi-org asset management: centrally managed assets in one system but with the capability to create multiple, independent asset databases, each with access and visibility controls. By default, there are no partitions, so asset management acts like it does currently. Once you add one or more partitions, it takes on a new more flexible approach.

[Explain the complexity that needs to be understood]

If your instance does not have partitions, then anyone with assets as a viewer or assets manager has access to all the assets. In Configuration, admins can create one or more partitions (**Service Manager > Assets > Manage Partitions**), and each asset record can be allocated to one, and only one, partition. The alternative, once enabling partitions on your instance, it to allocate asset records to Un-partitioned Assets, which treats those asset records as if there were no partitions enabled. The allocation is the same for asset types and asset categories; types and categories are allocated to one, and only one, partition. Each partition has visibility controls to establish who (individual users or groups) has access to the assets as either viewers or asset managers. As the name partition implies, no one (outside of a superuser looking at the database) can have a view on assets from more than one partition at a time.

the ability to facilitate MSP or Multi-Org asset management. That is, centrally managed assets in one system but with the ability to create multiple, independent asset databases, each with access and visibility controls.  We call this "Partitioning" and this demo shows how this works.  It's been designed that, by default, there are no partitions so it acts like it does currently, once you add one or more partitions it takes on a new more flexible (but also more complex understanding required). 

RQ-SM-0033/4 - Asset Partitioning and Visibility Controls
At the moment, the Asset Database is one single database, if you have access to assets as either an analyst (viewer) or an asset manager (viewer/writer) then you have access to all assets. The requirement here is to implement a scheme to partition assets. In essence, in administration we will be able to 



## Before you begin
To access the Asset Management capabilities of Hornbill Service Manager as an admin, your user account must have the following role associated:

|**To do this**|**You need this role assigned**|
|:----|:----|
|Add partitions to an instance|Asset Management Admin|

To work with partitions, you must enable an application setting:
|**To do this**|**You need to enable this ___**|
|:----|:----|
|Add partitions to an instance|`asset.partitioning.enable`
|

