---
title: Create and manage partitions
layout: article
keywords: visibility of assets
---
# Overview

::: note
This article is new, to support the preview release of the new Asset Management and its new UI.
:::

<!--Partitions facilitate asset management by providing asset managers and asset viewers the required segregation and subsequent visibility controls. As an assets admin, you can see all the partitions and asset records, or, you may be restricted from seeing certain partitions and their records.-->

Asset management in Hornbill provides the ability to facilitate multi-org asset management: centrally managed assets in one system but with the capability to create multiple, independent asset databases, each with access and visibility controls. By default, there are no partitions in your asset management implementation; once you add one or more partitions, your implementation takes on a more flexible approach.

If your instance does not have partitions, then anyone with the Asset Management Admin role or the Asset Management User role has access to all the asset records.

In Configuration, admins can create one or more partitions (**Service Manager > Assets > Manage Partitions**), and each asset record can be allocated to one, and only one, partition. The alternative, if you don't want that one-and-only-one restriction, is to allocate asset records to *Un-partitioned Assets*. That allocation treats asset records as if there were no partitions enabled. (The *Un-partitioned Assets* allocation is only visible once you have enabled partitions on your instance.)

The partition allocation is the same for asset types and asset categories; types and categories are allocated to one, and only one, partition. Each partition has visibility controls to establish who has access to the assets as either viewers or asset managers. <!--As the name *partition* implies, no one (outside of a superuser looking at the database) can have a view on assets from more than one partition at a time.--> You restrict access to partitioned records by [user, group, or role](/servicemanager-config/assets/manage-partitions#managing-access-to-partitions).

## Before you begin
When accessing the Asset Management capabilities of Hornbill Service Manager as an admin, first make sure your user account has the correct role associated, and make sure your instance is enabled for partitions.

|**To do this**|**You need this role assigned**|**You need to enable this setting:**
|:----|:----|:----|
|Add partitions to an instance|Asset Management Admin|`asset.partitioning.enable`|

::: important
Make sure you [understand the implications of partitioning assets](/servicemanager-config/assets/manage-partitions#deciding-whether-to-create-partitions) before you create partitions in your Hornbill instance.
:::

## Deciding whether to create partitions
Only partition your assets if you have a strong reason to do so.

There are various places in Hornbill where assets can be viewed and acted upon by users who do not have the Asset Management Admin role or the Asset Management User role. For example, when agents log a request, they may need to select an asset as part of that process in the Intelligent Capture.

In the case of a managed service provider (MSP), that Intelligent Capture is designed for a specific set of users. Each service is defined separately for each customer. The service defines an Intelligent Capture, and the Intelligent Capture --- by prompting the user for an asset --- defines which asset partition they can search and select from. The form filters further based on ownership, shared visibility, and so on.

As an assets admin, you control Asset Management users' access to partitioned asset records by role, group, or user --- but not to individual integration points such as the search form in an Intelligent Capture.

If you choose to enable partitioning, you must revisit all your Intelligent Captures that use the Asset form and change this to the Partitioned Assets form.

In terms of access to partitions for agents, you only need to [set up access to partitions](/servicemanager-config/assets/manage-partitions#managing-access-to-partitions) to those agents who need to view and manage the full asset record. If agents do not have permission to view an asset, they can still see the asset in related asset lists (e.g. in a request). But if they try to view the record, they will get an access error.

## Creating partitions
You create and manage partitions in **Configuration > Service Manager**. Asset Management users can then work with assets within those partitions in **Service Management > Assets**.

On a per-user basis, the partition selected by any user is saved. When that user goes back into Asset Management, they view that same partition again. This remembering of the users' selections can be deactivated using the application setting `asset.partition.current`.

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

Now you can [add asset categories to your new partition, or move un-partitioned assets](/servicemanager-config/assets/manage-partitions#organizing-assets-in-partitions) into it.

## Managing access to partitions
When working with a partition in **Manage Partitions**, you can configure permissions to control who has access and what they can do with that access.

::: important
If you don't define any access permissions, anyone who has access to view assets will see that partition.

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

    Your changes take effect for your chosen users when they refresh their browser or log out and back in.

## Organizing assets in partitions
Once you have enabled partitions on your instance and created partitions, it's time to organize the assets they'll contain. You can create new categories and types in the partition, move un-partitioned assets into the partitions, or move assets from one partition to another partition.

**To add a new asset category into a partition:**
1. In **Configuration > Service Manager > Assets > Manage Types**, from the Partitions dropdown, select the partition you want to work with.
1. In the Asset Categories row, click **Add new category** (the plus sign).
1. Give the category a name.
1. (Optional) Enter a description.
1. Click **Create**.

You can now add new asset types in the category you have created.

You can create asset categories and asset types with the same name in different partitions. You cannot, however, move a type to a different partition if there is already a type of the same name there. If you move a category to a different partition that already has a category of the same name, the two categories are merged into one.

**To move an asset category into a partition:**
1. In **Configuration > Service Manager > Assets > Manage Types**, click the category name.
1. Under the list of available asset list columns, click **Move to Partition**.
1. In the Migrate Category dialog, from the dropdown, select the partition you want to move the category to.
1. Click **Migrate**.

**To move an asset type into a partition:**
1. In **Configuration > Service Manager > Assets > Manage Types**, click the type name.
1. In the General tab, at the bottom of the view, click **Move to Partition**.
1. In the Migrate Type dialog, from the first dropdown, select the partition you want to move the category to.
1. From the second dropdown, select the category you want to move the type to.
1. Click **Migrate**.

<!-- ## Changing the Asset form for Intelligent Captures

NWJ said "in non-asset ui view, there is no option to filter by partition but rather it picks up the partition to filter by automatically using **a new setting in catalog service** (so a raised request in essence is related to a partition so any asset filtering on a request is based on that)."-->

<!--ANOTHER QUESTION: Can multiple partitions be selected on a service?

[IS THIS PARAGRAPH WRONG NOW? IS IT THE HORNBILL ADMIN, NOT THE ASSET ADMIN, WHO DETERMINES WHICH END USERS CAN SEE ASSET RECORDS?] As an asset admin in charge of partitioned assets, you determine which end users see asset records. You do this when you set up a service to use a partition or when you set up an Intelligent Capture to use a partition. Then, when logging a request, the end user can select only assets from that partition.

Service Manager users can see assets when logging or viewing requests. This is because the request itself is linked to a partition. <!--That way you don't have to set up every analyst to have specific permissions on partitions.If a user clicks the hyperlink to access the asset record, then partition access is required i.e. a helpdesk analyst wont be able to access record/view.-->