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

?? Will customers want to know how filtering works when assets are partitioned? Or maybe the question is this: HOW DO USERS WHO ARE NOT ASSET MGMT USERS SEE ASSETS (e.g. those related to a request, or for non-SM users using the Employee Portal and seeing asset lists in an Intelligent Capture).
A raised request is related to a partition through a setting in the service that the request is raised against. Asset filtering is based on that.
<!--funny story we went through and add filtering to most parts but are now reworking so in non asset ui view there is no option to filter by partition but rather it picks up the partition to filter by automatically using a new setting in catalog service (so a raised request in essence is related to a partition so any asset filtering on a request is based on that)... basically servicedesk analysts won't even be aware of partitions-->
BD: @NWJ Would it be a single partition per service, or could multiple partitions be selected?

## Before you begin
When accessing the Asset Management capabilities of Hornbill Service Manager as an admin, first make sure your user account has the correct role associated, and make sure your instance is enabled for partitions.

|**To do this**|**You need this role assigned**|**You need to enable this setting:**
|:----|:----|:----|
|Add partitions to an instance|Asset Management Admin|`asset.partitioning.enable`|

## Creating partitions
You create and manage partitions in **Configuration > Service Manager**. Asset Management users can then work with assets within those partitions in **Service Management > Assets**.

**To create a partition:**
1. Navigate to **Configuration > Service Manager > Assets > Manage Partitions**.
    ::: tip
    If you don't see **Manage Partitions** under **Assets**, you need to enable the application setting `asset.partitioning.enable`.
    :::
1. In the partitions list, click **+ New Partition**.
1. Give the partition an ID, or click **Auto ID**.
1. Give the partition a name.
1. (Optional) Enter information in the Summary field.
1. Navigate to **Service Management > Assets**.
1. In the Partitions dropdown above **Dashboard** and **All Assets**, click the down arrow to view your new partition in the list.
1. Click your new partition's name to go to its dashboard.

## Managing access to partitions
When working with a partition in **Manage Partitions**, you can configure permissions to control who has access and what they can do with that access.

::: note
The permissions you grant are overridden by the users’ asset role permissions. For example, if the users’ role does not allow them to delete assets, then they cannot delete assets even if you allow deleting.
:::

**To manage access to a partition:**
1. Navigate to **Configuration > Service Manager > Assets > Manage Partitions**.
1. In the partitions list, click the name of the partition you want to manage.
1. In the *Partition Access* section, click **Add New**.
1. Use the first dropdown to grant access by role, group, or user.
1. Use the second dropdown to add further filtering to the access granted.
1. Use the third dropdown to specify whether the access allows viewing only; viewing, creating, and updating; viewing, creating, and deleting; or all of those actions.
1. Save your changes (click the icon next to the third dropdown).