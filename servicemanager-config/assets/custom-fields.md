---
layout: article-toc
---

# Common custom fields

:::note
[[INCLUDE https://raw.githubusercontent.com/Hornbill-Docs/hdoc-library/main/hdoc-library/service-manager/new-assets-note.md]]
:::

Common fields are fields that are shared across all [classes](/servicemanager-config/assets/asset-structure#asset-classes) of asset. They include both standard fields and custom fields. These custom fields are know as *common custom fields*.

When defining [asset types](/servicemanager-config/assets/manage-asset-types#asset-types), you will be able to select from these common custom fields to include in either the summary or detail view or when creating an asset of that type.

## Control types

There are 5 different control types for common custom fields:

* **text**: A single line of text.
* **integer**: A whole number.
* **decimal**: A number that can include a decimal point.
* **datetime**: A date and time value.
* **textarea**: Multiple lines of text.

Each control types has 15 custom fields available, other than the **textarea** control type, which has 5 custom fields available.

## Renaming custom fields

For a common custom field, you will want to provide a name that is displayed to users when they see the field in the UI. This is done under the translation column of the common custom fields list. This allows you to give the field a name that is relevant to any asset that uses this field, and to change the name of the field for different languages.

**To change the name of a shared custom field:**

1. Navigate to **Configuration > Service Manager > Assets > Common Custom Fields**.
1. In the Translated column for the custom field you want to change, click the custom field's name.
1. Enter the new display name and click **Save**.
1. *(Optional)* To provide a name in a different language, select the language from the dropdown and enter the name in the translation column for that language, then click **Save**.
