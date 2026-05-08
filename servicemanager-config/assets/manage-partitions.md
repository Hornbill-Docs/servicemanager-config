---
layout: article
keywords: visibility of assets
---
# Asset partitions

:::note
[[INCLUDE https://raw.githubusercontent.com/Hornbill-Docs/hdoc-library/main/hdoc-library/service-manager/new-assets-note.md]]
:::

Asset partitioning allow you to divide your company's assets into separate, individual units. You can partition assets to provide an additional layer that enforces access and visibility controls.

* **Improved security controls**: Partitioning allows sensitive assets to be segregated, enabling stricter security controls and improved protection against unauthorized access.
* **Targeted incident response**: partitioning helps teams identify specific assets affected by an incident.

## Before you begin

* Watch the following video for an explanation of partitioning, how it works in practice, and how to set up and use partitions.

    <iframe width="560" height="315" src="https://www.youtube.com/embed/V-_Bp19m4Ek?si=KqC5-zV7JwHPEQn5" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
    
* The following role is required.

    |Role|Description|
    |:----|:----|
    |Asset Management Admin|Can manage all aspects of asset management, including creating and managing partitions|

## Understanding partitions

Here are a few important facts about partitioning assets in Hornbill:

* **Each asset record can only be allocated to one partition**. You cannot allocate an asset to more than one partition.
* **Types and categories can also only be allocated to one partition**. But asset types and asset categories can exist with the *same names* in multiple partitions.
* **Unpartitioned Assets**. Assets not assigned to a specific partition will reside in the unpartitioned asset container. The *Un-partitioned Assets* allocation is only visible once you have enabled partitions.
* **Work on one partition per browser tab**. Asset managers and viewers can see assets from only one partition at a time. To work on multiple partitions side by side, open multiple browser tabs.
* **Restricting access**. You restrict access to partitioned records by user or role.
* **Partitioning is not backwards compatible**. This means that it only applies to requests logged after a partitions is created, as the Partition ID is assigned during request creation.

<!-- JE: This is CM's original bullet for above. Leaving it here for now in case I've got something in the wording wrong in my rewrite.
** When partitions are used for some assets, other assets can co-exist outside of partitions. These are recorded as *Un-partitioned Assets*. The *Un-partitioned Assets* allocation is only visible once you have enabled partitions.


* **Visibility controls**. Each partition has visibility controls to establish who has access to the assets as either viewers or asset managers.

* **Work on one partition per browser tab**. Asset managers and viewers can see assets from only one partition at a time. To work on multiple partitions side by side, open multiple browser tabs.

* **Restricting access**. You restrict access to partitioned records by [user or role](/servicemanager-config/assets/manage-partitions#managing-access-to-partitions).

* **Partitioning is not backwards compatible**. This means that tt only applies to requests logged after the partitions were created, as the Partition ID is assigned during request creation.

-->

## Deciding whether to create partitions

Only partition your assets if you have a strong reason to do so.

Partitioning is useful when:

1. You manage assets across multiple departments in your organization and you want to restrict access to set of assets.
2. You are a Multi-Service Provider (MSP) and oversee assets spanning different organizations and Hornbill instances.

If you choose to enable partitioning, for all forms where you wish to enforce partitioning visibility you must revisit all your Intelligent Captures that use the Asset form and change this to the Partitioned Assets form.

## Create and use partitions

There are three stages to creating and applying a partition for it to be used:

1. Create a partition and assign access.
1. Add assets to the partition.
1. Update forms and apply service association.

The next sections explain each stage.

## Create a partition and assign access

**To create a partition:**

1. Navigate to **Configuration > Service Manager > Assets > Manage Partitions**.
1. In the partitions list, click **+ New Partition**.
1. Give the partition an ID, or click **Auto ID**.
1. Give the partition a name.
1. (Optional) Enter information in the Summary field.
1. Navigate to **Service Management > Assets**.
1. In the Partitions dropdown above **Dashboard** and **All Assets**, click the down arrow to view your new partition in the list.
1. Click your new partition's name to go to its dashboard.


### Manage partition access 

When working with a partition in **Manage Partitions**, you can configure permissions to control who has access and what they can do with that access.

::: important
If you don't define any access permissions, anyone who has access to view assets will see that partition.

The permissions you grant are overridden by the users’ asset role permissions. For example, if the users’ role does not allow them to delete assets, then they cannot delete assets even if you allow deleting.
:::

As an assets admin, you control Asset Management users' access to partitioned asset records by security or user role.

Grant access to partitions to agents who need to view and manage full asset records.

If an agent does not have permission to view an asset, they can still see the asset name in related lists, such as within a request. However, the system displays an access error if the agent attempts to open the record to view its full details.

**To manage access to a partition:**

1. Navigate to **Configuration > Service Manager > Assets > Manage Partitions**.
1. In the partitions list, click the name of the partition you want to manage.
1. In the *Partition Access* section, click **Add New**.
1. Use the first dropdown to grant access by role or user.
1. Use the second dropdown to add further filtering to the access granted.
1. Use the third dropdown to specify whether the access allows viewing only; viewing, creating, and updating; viewing, creating, and deleting; or all of those actions.
1. Save your changes (click the icon next to the third dropdown).

    Your changes take effect for your chosen users when they refresh their browser or log out and back in.

## Add assets to the partition

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
1. In the Move Category dialog, from the dropdown, select the partition you want to move the category to.
1. Click **Move**.

**To move an asset type into a partition:**

1. In **Configuration > Service Manager > Assets > Manage Types**, click the type name.
1. In the General tab, at the bottom of the view, select **Move to Partition**.
1. In the Move Type dialog, from the first dropdown, select the partition you want to move the category to.
1. From the second dropdown, select the category you want to move the type to.
1. Select **Move**.

## Update forms and apply service association

### Enable partitions in Intelligent Capture forms

When a user fills out a form to raise a request, you can limit their view to a single partition of assets. This ensures they only see and select items that apply to their needs.

To restrict asset visibility, use the Partitioned Assets form within the Intelligent Capture Designer. 

If you have an existing form that uses the standard Assets form, you must replace it with the Partitioned Assets form to enable partitioning for asset selection in the form.

#### Configuration options

The Partitioned Assets form includes all the settings available in the standard Assets form, plus an additional option for partitions:

* Partition selection: Choose the specific partition you want to display to the user, from **Filter by Partition**.

As with the Assets form, you can use the other options to further narrow down the items available within the selected partition.

![Screenshot showing the Partitioned Assets form options in the Intelligent Capture Designer](/_books/servicemanager-config/assets/images/partitioned-assets-form.png)

### Associate a partition to a service

This is done within the Service Manager application.

From the the Service Portfolio, navigate to a service's configuration settings and assign a partition from the **Asset Partition Filter** menu.

![Screenshot showing the Asset Partition Filter](/_books/servicemanager-config/images/asset-partition-filter.png)

<!--Cammy QUESTION: Can multiple partitions be selected on a service. Joel: No?

[IS THIS PARAGRAPH WRONG NOW? IS IT THE HORNBILL ADMIN, NOT THE ASSET ADMIN, WHO DETERMINES WHICH END USERS CAN SEE ASSET RECORDS?] As an asset admin in charge of partitioned assets, you determine which end users see asset records. You do this when you set up a service to use a partition or when you set up an Intelligent Capture to use a partition. Then, when logging a request, the end user can select only assets from that partition.

Service Manager users can see assets when logging or viewing requests. This is because the request itself is linked to a partition. <!--That way you don't have to set up every analyst to have specific permissions on partitions.If a user clicks the hyperlink to access the asset record, then partition access is required i.e. a helpdesk analyst wont be able to access record/view.-->