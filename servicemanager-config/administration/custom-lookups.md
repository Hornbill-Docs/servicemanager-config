---
layout: article-toc
---
# Custom lookups
Custom lookups allow you to define sets of records that associate values together.  

For example, you can associate a specific catalog item with a supporting team. These records of association do not need to be created within workflows and can simply be called into a process at the point of need. As a result, custom lookups remove the need for using Decision nodes to route information for separate tasks. Instead, a single task, usually within a Hornbill Automation node, can be used.

## Topics covered
* [Before you begin](/servicemanager-config/administration/custom-lookups#before-you-begin)
* [Creating custom lookups](/servicemanager-config/administration/custom-lookups#creating-custom-lookups)
* [Using custom fields in custom lookups](/servicemanager-config/administration/custom-lookups#using-custom-fields-in-custom-lookups)
* [Using custom lookups in workflows](/servicemanager-config/administration/custom-lookups#using-custom-lookups-in-workflows)
* [Further learning](/servicemanager-config/administration/custom-lookups#further-learning)

## Before you begin
You must have the Service Desk Admin role to create and manage custom lookups.

## Creating custom lookups 
A custom lookup can contain one or more records of associations.

When creating a custom lookup, you can associate records from a list of existing entities, or you can use [custom fields](/servicemanager-config/administration/custom-lookups#using-custom-fields-in-custom-lookups) to give yourself further configuration options.

**To create a custom lookup:**
1. In [Configuration](/esp-config/getting-started/using-configuration), navigate to **Service Manager > Administration > Custom Lookups**.
1. In the Custom Lookups list view, click the **Add** button (the plus sign).
1. Give the new custom lookup a name and a description.
1. (Optional) Change the status from the default Active to Offline.
    ::: note
    If you are going to use the custom lookup in a workflow, make sure the status is set to Active.
    :::
1. Click **Create**.

**To associate a record to a custom lookup:**
1. In the list of custom lookups, click the **View** button (the eye icon) in the row of the custom lookup you want to configure.
1. In the Details & Records view, go to the Records tab.
1. Click the **Add** button (the plus sign) to create a new record.
1. In the Reference field, give the new record a name.
1. In the Configurations section to the right, click the down arrow to access the *Please select an entity* dropdown.
1. Select an entity.
    1. (Optional) If the entity you want is not in the list, you can use a custom field to make it available. See [Using custom fields in custom lookups](/servicemanager-config/administration/custom-lookups#using-custom-fields-in-custom-lookups).
1. Click **Create**.

## Using custom fields in custom lookups
Within each custom lookup, you define a set of one or more associated records. To do this, select the eye icon on the custom lookup entry to access the Custom Lookup Details and Records tabs. For creating records of association in custom lookups, Custom Fields 1 through 5 are reserved and available to use.

**To create a record for use in a custom lookup:**
1. In the list of custom lookups, find the row of the custom lookup you want to configure, and click the **View** button (the eye icon).
1. In the Details & Records view, go to the Details tab.
1. In the list of custom fields (or if the list is empty, where it says *No Custom Fields Defined...*), click the **Add** button (the plus sign).
1. In the **Field** dropdown, select one of the available custom fields.
1. (Optional) In the Label field, give the record a name. This name will appear in the *Please select an entity* dropdown when associating a record to a custom lookup.
1. Click **Update**.

When you create a record, the following settings and fields are available:
- **Reference.** The name of the associated record.
- **Status.** This specifies whether the record will be applied when the custom lookup is used in a workflow. Choose either Active (for use in a workflow) or Offline.
- **Entity.** The entity that is associated with the reference. There are a number of entities available to select from the dropdown, such as Approver, Request Category, and Risk. If you need more options, you can use Custom Fields 1 to 5 to add more as described above.
- **Value.** The entity value that is associated with the reference.

## Using custom lookups in workflows
You can use custom lookups in workflows as a way of invoking pre-defined associations when performing automations. For example, when performing team assignment in a workflow, you can use a custom lookup record to automatically assign a specific team to all requests that were raised against a specific catalog item. This is because the record contains an association between the catalog item and the team. 

 To use a custom lookup in a workflow, add a Hornbill Automation node with these settings: 

- Application: Service Manager 
- Scope: Entity 
- Entity: Custom Lookups 

The Type and Task fields will auto-populate with the default settings. 

In subsequent nodes, you can use the variable picker to inject custom lookup entities.

:::important
When assigning a team using a custom lookup, in the Hornbill Automation node that follows the custom lookup, make sure the input parameter Team contains the Team ID, not the team name.
:::



## Further learning 
Watch this video for an overview on how to use Custom Lookups to improve your Workflows.

<iframe width="560" height="315" src="https://www.youtube.com/embed/0H3r9eYI3Mg?si=GRCUjXgd8circRSp" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>