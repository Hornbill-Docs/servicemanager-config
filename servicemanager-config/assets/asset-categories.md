---
layout: article-toc
---

# Asset categories

Asset Categories allow you to group asset types into logical categories. The Asset Categories panel shows each category and their associated asset types.

![Asset Categories Panel](/_books/servicemanager-config/images/asset-categories-panel.png)

From the asset categories list you can:

* Create a new category by clicking on the `+` button in the title bar.
* Select an existing category to view the properties of that category.
* To the right of the category name, click on the `+` to add a new asset type under that category.
* Select an existing asset type to view the properties of that asset type.
* Drag-and-drop asset types between categories.

## Uncategorized

Any asset type without a category will be listed under **Uncategorized**. If there are no uncategorized asset types, this option will not be available. From this list, you can drag-and-drop an asset type onto an appropriate category.

Alternatively, by clicking on the Uncategorized title, suggested categories are provided for each uncategorized asset type. Clicking on the `Create and Assign` button will create the new suggested category and add the selected asset types to that category.

:::note
Category selection is mandatory on new asset types.  Only the asset types that were created prior to the introduction of categories will be displayed in this list.
:::

## Asset category details

When you select a category, you can view and edit the details of that category in the right panel.

### Available asset list columns

The **Available Asset List Columns** section allows you to choose which fields are available to users when viewing a list of assets by category.

#### Use Class Defaults

![Use Class Defaults button](/_books/servicemanager-config/images/assets-use-class-defaults-button.png)

Selecting this button will reset the list of available fields with the default fields for the asset class associated to the category. This action can't be undone.

#### Category Common field

![Common field](/_books/servicemanager-config/images/assets-common-field-button.png)

Common fields are fields that are shared by all assets. When you add a common field as an available column, users will be able to view this column as part of their category asset list.

## Archiving asset categories

Archiving helps you manage your asset library by restricting access to older items and preventing the creation of new assets in archived categories.

When you archive a category, the system does not delete any data. Instead, it changes the state to archived.

When a category or type is archived, this becomes the unarchive button.

### Archive an asset category

1. Navigate to the **Manage Types** page.
2. Select the category you want to archive from the left-hand menu.
3. Select the **Archive** button.
4. Choose an archive mode:
   * **Category only**: Archives only the category name.
   * **Category & types**: Archives the category and all asset types within it.
   * **Category, types, and assets**: Archives the category, its types, and all associated assets.
5. If you choose to archive assets, review the per-type and per-state breakdown.
6. Select a sub state for each row as needed.
7. Confirm the action to complete the process.

### Unarchive an asset category

1. Select the archived item in the navigation tree.
2. Select the **Unarchive** button.
3. Choose the unarchive mode that matches your needs (such as **Type only** or **Type & assets**).
4. If you unarchive assets, review the groups organized by their current sub state.
5. Pick a new state and an optional new sub state for each group you want to restore.
6. Confirm the changes.
