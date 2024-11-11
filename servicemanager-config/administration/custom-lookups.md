---
layout: article-toc
---
# Custom Lookups
Custom Lookups allow you to define sets of records that associate values together.  

For example, you can associate a specific catalog item with a supporting team. These records of association do not need to be created within Workflows and can simply be called into a process at the point of need. As a result, Custom Lookups remove the need for using Decision nodes to route information for separate tasks. Instead, a single task, usually within a Hornbill Automation node, can be used.

## Topics Covered
* [Before You Begin](/servicemanager-config/administration/custom-lookups#before-you-begin)
* [Creating Custom Lookups](/servicemanager-config/administration/custom-lookups#creating-custom-lookups)
* [Creating Records](/servicemanager-config/administration/custom-lookups#creating-records)
* [Using Custom Lookups in Workflows](/servicemanager-config/administration/custom-lookups#using-custom-lookups-in-workflows)
* [Further Learning](/servicemanager-config/administration/custom-lookups#further-learning)

## Before You Begin
You must have the Service Desk Admin role to create and manage Custom Lookups.

## Creating Custom Lookups 

A Custom Lookup can contain one or more records of associations.

When you create a Custom Lookup, the following settings and fields are available:
- **Name.**
- **Description.**
- **Reference Type.** This determines the item that you associate to a value.
- **Status.** Choose either Active or Offline.

## Creating Records
Within each Custom Lookup, you define a set of one or more records. To do this, select the eye icon on the Custom Lookup entry to access the Custom Lookup Details and Records tab. 

When you create a record, the following settings and fields are available:
- **Reference.** This dropdown provides you with options of the reference type specified in the Custom Lookup. For example, if you specified a Service Catalog Item, the dropdown will display a list of your catalog items.  
- **Status.** This specifies whether the record will be applied when the Custom Lookup is used in a Workflow. Choose either Active or Offline.
- **Entity.** This defines the type of entity that is associated with the reference type.
- **Value.** This defines the entity value that is associated with the reference type.

## Using Custom Lookups in Workflows
You can use Custom Lookups in Workflows as a way of invoking pre-defined associations when performing automations. For example, when performing team assignment in a Workflow, you can use a Custom Lookup record to automatically assign a specific team to all requests that were raised against a specific catalog item. This is because the record contains an association between the catalog item and the team. 

 
 To use a Custom Lookup in a Workflow, add a Hornbill Automation node with these settings: 

- Application: Service Manager 
- Scope: Entity 
- Entity: Custom Lookups 

The Type and Task fields will auto-populate with the default settings. 

In subsequent nodes, you can use the variable picker to inject Custom Lookup entities.

:::important
When assigning a team using a custom lookup, in the Hornbill Automation node that follows the custom lookup, make sure the input parameter Team contains the Team ID, not the team name.
:::



## Further Learning 

[Watch this video](https://youtu.be/0H3r9eYI3Mg) for an overview on how to use Custom Lookups to improve your Workflows. 