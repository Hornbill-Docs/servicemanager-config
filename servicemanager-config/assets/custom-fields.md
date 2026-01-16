---
layout: article-toc
---

# Using custom fields

::: note
This document covers the [preview release](/servicemanager-config/assets/overview#preview-visibility) of the new asset management features and user interface. You can find documentation for the current UI [here](/servicemanager-user-guide/asset-management/overview).
:::

When configuring an asset type to customize your users’ view of assets, you can choose one or more custom fields (for use with that type). You can also change the display names for custom fields; this is done in [two different ways](/servicemanager-config/assets/custom-fields#adding-and-renaming-custom-fields-for-assets). 

The custom fields are available in **Configuration > Manage Types**, from the dropdowns in the **Summary Fields**, **Detail Fields**, **Create Fields** and **List Fields** tabs. You can also access and add custom fields for an entire category. You can choose from field types of *Varchar*, *Integer*, *Decimal*, *Date*, and *Text*.

## About shared fields versus class-specific fields
A large number of fields --- including custom fields --- are available and shared across all asset classes. The shared fields are called *common fields*. These shared fields can be chosen from the **+ Common field** dropdown. It is the dropdown *to the right of* this dropdown from which you choose class-specific fields.

### Common custom fields
Common custom fields can be used in every single class, including the General class. Despite the name *General*, do not confuse fields in the General class with common fields; General fields are specific to the General class and you add them from the **+ General field** dropdown.

In the **+ Common field** dropdown, you can't select a custom field that's already in use --- it will no longer be available in the dropdown list.

::: important
Because some common custom fields used in your implementation are likely to be shared, keep in mind that different asset types might each have a different purpose or meaning for a certain field's use. For this reason, if you are doing reporting that includes any common custom fields, be careful.
:::

### Class-specific custom fields
Non-shared custom fields can be chosen from the class-specific dropdown for the asset type you are working with (e.g. by clicking the **+ Computer system field** button.)

Class-specific custom fields are extended attributes to an assets table, with default names like *Ext.Custom Varchar 1*.

## Adding and renaming custom fields for assets

You can change the name of a class-specific custom field when adding it. You can also change its name in **Configuration > Service Manager > Assets > Common Custom Fields**. The **Common Custom Fields** view is also where you must go to change the name of a common custom field.

::: note
If others in your organization also have the Asset Management Admin role, they can change the display name you have entered, or revert the custom field's name to the default.
:::

**To add a custom field:**
1. In **Configuration > Manage Types**, click to select a category, or select a specific asset type and go to the **Summary Fields**, **Detail Fields**, **Create Fields** or **List Fields** tab.
1. In the list of columns or list of fields to show, click either the custom field dropdown (**+ Common field**) or the class-specific custom field dropdown, and select a custom field to add.
1. Configure the custom field. In the row of the newly added field, click the **Field Properties** button.
    1. If you're adding a custom field, then choose whether the field is read-only and mandatory.
    1. If you're adding a class-specific custom field, then give the field a custom label, and choose whether the field is read-only and mandatory.
1. Click **Apply**.

**To change the name of a shared custom field:**
1. Navigate to **Configuration > Service Manager > Assets > Common Custom Fields**.
1. In the Translated column for the custom field you want to change, click the custom field's name.
1. Enter the new display name and click **Save**.
1. *(Optional)* To revert the name back to its default, click the orange **Revert** button.
<!--
___
Common custom fields vs class/type custom fields.

**"Common custom fields" are NOT for the General asset class. They're common fields across all types/classes.**

The General asset class was like an asset class that ONLY had the shared attributes. 
CCF can be used in every single class inc. the General class.
The General class is there for asset types that don't fit into any ones we don't provide ootb.

Class-specific custom fields are extended attributes to a __ table, with default names like *Ext.Custom Varchar 1*.

*There are custom fields for the generic asset table and custom fields for asset classes.*

There are custom fields for each asset class, and there are custom fields that are shared across all assets (a.k.a. *common custom fields*).

You can't re-label shared custom fields by type.

In the **+ Common field** dropdown, you can't select a custom field that's already in use b/c it is no longer available in the dropdown list.

**To configure a common custom field:**
Properties dialog
1. Read-only (yes/no)
1. Mandatory (yes/no)
1. Cancel or Apply

**To configure a class-specific custom field:**
Properties dialog
1. Custom Label
1. Read-only (yes/no)
1. Mandatory (yes/no)
1. Cancel or Apply

___-->