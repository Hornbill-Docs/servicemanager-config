---
layout: article-toc
---
# Custom lookups
Custom lookups are a type of lookup table that can be used in a workflow to look up a reference record, which in turn, provides one or more values back to the workflow.  The Custom Lookups work in conjunction with the [Custom Lookup Workflow Automation](/servicemanager-config/customize/workflows/custom-lookup-automation). 

```mermaid
flowchart LR
    A[Custom Lookup Automation]
    A --> B[Find Custom Lookup]
    B --> C[Find Reference Record]
    C --> D[Return Reference Values]
```
Custom lookups can remove the need for complex [decision nodes](/esp-config/automation/decision) in a workflow, where a series of nested decision nodes can be replaced with a single Custom Lookup Automation. 

## Topics covered
* [Before you begin](/servicemanager-config/administration/custom-lookups#before-you-begin)
* [Creating custom lookups](/servicemanager-config/administration/custom-lookups#creating-custom-lookups)
* [Using custom fields in custom lookups](/servicemanager-config/administration/custom-lookups#using-custom-fields-in-custom-lookups)
* [Using custom lookups in workflows](/servicemanager-config/administration/custom-lookups#using-custom-lookups-in-workflows)

## Before you begin
- The [Service Desk Admin](/servicemanager-config/setup/service-manager-roles#administration-roles) role is needed to create and manage custom lookups.
- The [Business Process Manager](/esp-config/organizational-data/roles#system-roles) role is needed to access workflows to add the Custom Lookup Automation.
- Be familiar with general [workflow automation](/servicemanager-config/customize/workflows/using-workflows-with-service-manager). 

## Creating custom lookups 
### Step 1: Add a custom lookup
A custom lookup is a container that holds multiple reference records.  The name of the custom lookup will be used by the [Custom Lookup Workflow Automation](/servicemanager-config/customize/workflows/custom-lookup-automation) to identify the list of reference records that it will use. The status should be set to **Offline** until the configuration has been completed.

1. In [Configuration](/esp-config/getting-started/using-configuration), navigate to **Service Manager > Administration > Custom Lookups**.
1. In the Custom Lookups list view, click the `+` button located in the top right.
1. Give the new custom lookup a name and a description.
1. Click **Create**.

### Step 2: Add a reference record
The reference name is key to providing a match for the [Custom Lookup Automation](/servicemanager-config/customize/workflows/custom-lookup-automation).  The Custom Lookup Automatomation will look throught all the references on a Custom Lookup for a matching reference and then pass the values for that reference back to the workflow.

1. In the list of custom lookups, click the **View** button (the eye icon) in the row of the custom lookup you want to configure.
1. Select the `Records` tab.
1. Click the **Add** button (the plus sign) to create a new record.
1. In the Reference field, give the new record a name.
1. In the Configurations section to the right, click the down arrow to access the *Please select an entity* dropdown.
1. Select an entity.
1. Click **Create**.


:::tip
If the entity you want is not in the list, you can use a custom field to make it available. See [Using custom fields in custom lookups](/servicemanager-config/administration/custom-lookups#using-custom-fields-in-custom-lookups).
:::

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
- **Entity.** The entity that is associated with the reference. There are serveral entities available to select from the dropdown, such as Approver, Request Category, and Risk. If you need more options, you can use Custom Fields 1 to 5 to add more as described above.
- **Value.** The entity value that is associated with the reference.

## Using custom lookups in workflows
You can use custom lookups in workflows as a way of invoking pre-defined associations when performing automations. For example, when performing a team assignment in a workflow, you can use a custom lookup record to automatically assign a specific team to all requests that were raised against a specific catalog item. This is because the record contains an association between the catalog item and the team. 

 **To use a custom lookup in a workflow:**
 1. Add a Hornbill Automation node with these settings:

    Application: Service Manager

    Scope: Entity

    Entity: Custom Lookups

    (The Type and Task fields will auto-populate with the default settings.)

2. In the Options section, for Custom Lookup, use the dropdown to select your custom lookup.
3. In Reference (which refers to the record reference for the chosen custom lookup), manually set your reference to the name of the associated record. If the associated-records information is accessible using a variable, then use the [variable picker](/esp-config/automation/variable-picker) to select it.

When configured like this, what the Hornbill Automation node does is it loads the custom lookup reference entity values --- in the form of output parameters --- into the workflow, which can then be called from a subsequent node or nodes using the variable picker.

:::important
When assigning a team using a custom lookup, in the Hornbill Automation node that follows the custom lookup, make sure the input parameter Team contains the Team ID, not the team name.
:::
