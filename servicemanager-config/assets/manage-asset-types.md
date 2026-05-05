---
layout: article-toc
---

# Manage asset types

:::note
[[INCLUDE https://raw.githubusercontent.com/Hornbill-Docs/hdoc-library/main/hdoc-library/service-manager/new-assets-note.md]]
:::

Asset management within Hornbill Service Manager allows you to organize and present detailed information about each asset. By organizing assets into specific types, you can establish a comprehensive framework of fields and data tailored to each asset. This approach ensures that all relevant information is readily accessible for any asset.

## Before you begin

* The [Asset Management Admin role](/servicemanager-config/setup/service-manager-roles#asset-management-roles) is required to manage asset types and categories.
* Know how to access the [Service Manager Configuration](/servicemanager-config/index#access-service-manager-configuration).
* Understand how the [asset classes, types, and categories are structured](/servicemanager-config/assets/asset-structure).
* Decide whether you want to [enable asset partitions](/servicemanager-config/assets/manage-partitions) on your instance.

## Asset Categories

Asset Categories allow you to group asset types into logical categories. The Asset Categories panel shows each category and their associated asset types.

![Asset Categories Panel](/_books/servicemanager-config/images/asset-categories-panel.png)

From the asset categories list you can:

* Create a new category by clicking on the `+` button in the title bar.
* Select an existing category to view the properties of that category.
* To the right of the category name, click on the `+` to add a new asset type under that category.
* Select an existing asset type to view the properties of that asset type.
* Drag-and-drop asset types between categories.

### Uncategorized

Any asset type without a category will be listed under **Uncategorized**. From this list, you can drag-and-drop an asset type onto an appropriate category.

Alternatively, by clicking on the Uncategorized title, suggested categories are provided for each uncategorized asset type. Clicking on the `Create and Assign` button will create the new suggested category and add the selected asset types to that category.

### Asset Category details

When you select a category, you can view and edit the details of that category in the right panel.

#### Available Asset List Columns

The **Available Asset List Columns** section allows you to choose which fields are available to users when viewing a list of assets by category.

##### Use Class Defaults

![Use Class Defaults button](/_books/servicemanager-config/images/assets-use-class-defaults-button.png)

Selecting this button will reset the list of available fields with the default fields for the asset class associated to the category.

##### Category Common field

![Common field](/_books/servicemanager-config/images/assets-common-field-button.png)

Common fields are fields that are shared by all assets. When you add a common field as an available column, users will be able to view this column as part of their category asset list.

## Asset Types

To customize your users' view of assets, navigate to **Configuration > Service Manager > Assets > Manage Types**. Here you'll work in the following tabs:

### General

![General tab](/_books/servicemanager-config/assets/images/assets-general-tab.png)

In the General tab, you can set some of the basic information about the asset type and choose an icon or upload a custom image the will be used for all assets of this type.

* **Name**. The name of the asset that will be displayed everywhere assets are used.
* **Category**. The category for this asset type.
* **Description**. A description of this asset type.

#### Asset Card customization

The Asset Card is a like a business card that you can design for your asset. Key information of your choice can be added to the card. The defined asset card will appear on all assets defined under this asset type.

Here is an example of a summary card for an asset of the asset type Printer:

![Summary card for an asset](/_books/servicemanager-config/assets/images/assets-summary-card.png)

Where is the asset card displayed?

* When viewing an [asset detail record](/servicemanager-user-guide/asset-management/asset-details).
* When an asset is selected in the [Configuration Item Explorer](/servicemanager-user-guide/configuration-management/configuration-item-explorer).

There are options to customize the Summary Card and the Wide Summary card. The **Summary Card Editor** accepts HTML. Here you can include the values held in class custom fields. The syntax for this is:

- For common custom fields use `{{general.h_custom_char1}}`, replacing `char1` with the term in the custom field.
- For class specific fields use `{{extended.h_custom_ext_char1}}`, replacing `char1` with the term in the custom field.

To help you add the correct fields, a dropdown menu appears as you type the variable name in the editor, as this screenshot shows:

![Asset Summary Card editor dropdown](/_books/servicemanager-config/assets/images/asset-field-dropdown.png)

You can test how summary cards will be presented by selecting specific assets to preview in the summary card editor.

::: warning
When using the Summary Card Editor to customize asset summary cards, use *only* Hornbill-prescribed styles. Do not add your own styles; any other style declarations will be removed by Hornbill.
:::

### Summary fields

![Summary Fields tab](/_books/servicemanager-config/assets/images/assets-summary-fields-tab.png)

Go to the Summary Fields tab to choose the fields that a user sees when viewing an asset in the Summary view. The focus of an asset is put on this summary information when a user clicks on an asset in the asset list. You can customize the list of Summary fields so as to highlight the most important or most used fields for this type of asset.

Choose between a one-column or two-column layout of the fields. Use the **Quick Layout** button to choose to use default fields or legacy fields. Using legacy fields means Hornbill will read in your asset fields from your existing implementation.

Here is an example of a Summary view for an asset of the asset type Printer, using a one-column layout:

![Fields in an asset's Summary view](/_books/servicemanager-config/assets/images/summary-view-of-asset.png)

Here is the Summary view of the same asset, with fields configured in a two-column layout:
![Fields in an asset's Summary view, two-column layout](/_books/servicemanager-config/assets/images/summary-view-of-asset-2-column.png)

### Detail fields

![Detail Fields tab](/_books/servicemanager-config/assets/images/assets-detail-fields-tab.png)

In the Details view, users can access extended details beyond what is in the Summary view for an asset. Go to the Detail Fields tab to choose which fields you want users to see when viewing an asset in the Details view.

Choose between a one-column or two-column layout of the fields. Use the **Quick Layout** button to choose to use default fields or legacy fields. Using legacy fields means Hornbill will read in your asset fields from your existing implementation.

### Create fields

![Create Fields tab](/_books/servicemanager-config/assets/images/assets-create-fields-tab.png)

Go here to choose the fields available to a user when creating new assets. Use the **Quick Layout** button to choose to use default fields or legacy fields. Using legacy fields means Hornbill will read in your asset fields from your existing implementation.

Here is an example of a New Asset dialog when creating an asset of the asset type Printer:

![New Asset dialog](/_books/servicemanager-config/assets/images/create-new-asset.png)

### List fields

![List Fields tab](/_books/servicemanager-config/assets/images/assets-list-fields-tab.png)

Go to the List Fields tab to choose the fields that a user sees when viewing the list of assets in an asset type. You can drag the columns to change the order in which they appear in the list. Click the eye icon to toggle the columns from visible to hidden.

Here is an example of a what a users sees when viewing the list of assets by the asset type Printer:

![List view when viewing by asset type](/_books/servicemanager-config/assets/images/list-view-for-asset-type.png)

**Fields available for searching.** As an admin, you can configure the fields that are available for searching. If you want your users to be able to search for assets using specific fields, then add those fields here in the List Fields tab by adding additional columns. Once a column is added, it is available in the search.

**Fields available for CSV download.** The CSV download contains only the columns that you have added here in the List Fields tab.

## Archiving asset categories, types, and assets

Archiving helps you manage your asset library by restricting access to older items and preventing the creation of new assets in archived categories or types. 

When you archive an item, the system does not delete any data. Instead, it changes the state of the assets to archived. 

 When you archive assets, you can select specific asset state groups and sub states to include. The system does not affect any groups you do not select.

To archive asset categories, types, and their associated assets, select the archive button that appears when a category or type is selected in the left-hand menu, as highlighted here:

![asset type archive button](/_books/servicemanager-config/assets/images/asset-type-archive.png)

When a category or type is archived, this becomes the unarchive button.

### Archive an asset type

1. Navigate to the **Manage Types** page.
2. Select the asset type you want to archive from the left-hand menu.
3. Select the **Archive** button.
4. Choose an archive mode in the dialog box:
   * **Type only**: Archives only the asset type definition.
   * **Type & assets**: Archives the asset type and its associated assets.
5. If you choose **Type & assets**, select the asset state groups you want to archive. 
6. (Optional) Assign a sub state to each selected group.
7. Confirm the action to complete the process.

**Expected Result:** The asset type appears in italic text in the navigation tree. Users can no longer select this type when creating new assets.



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



### Unarchive an asset type or category

1. Select the archived item in the navigation tree.
2. Select the **Unarchive** button.
3. Choose the unarchive mode that matches your needs (such as **Type only** or **Type & assets**).
4. If you are unarchiving assets, review the groups organized by their current sub state.
5. Pick a new state and an optional new sub state for each group you want to restore.
6. Confirm the changes.


### Manage visibility of archived items

The system uses specific visual cues to help you identify archived records:
* **Navigation tree**: Archived categories and types appear in italic text. When you select a different item, the archived labels appear muted (faded).
* **Visibility toggle**: If you have asset management rights, go to **Service Manager** > **Assets**. Select the **eye icon** in the **Assets** title bar to show or hide archived items. 
   * An **open eye** icon means archived items are visible. 
   * A **closed eye** icon means archived items are hidden.
* **Permissions**: Users without asset management rights cannot see archived categories or types in the navigation tree.

### Audit archive events

You can also archive assets by updating the asset state directly in the asset editor within **Service Manager**. You can perform this action for one asset or multiple assets at the same time.

When you archive assets through the asset editor, you can choose to audit the update. Please note that the system does not support auditing when you archive items from the **Manage Types** page.


<!--

**To add a new asset type:**

1. Navigate to **Configuration > Service Manager > Assets > Manage Types**.
1. In the Asset Categories panel, find the category in which you want to create an asset type.
1. Next to the category name, click **+** (the plus sign).
1. Give the new type a name.
1. From the dropdown, select an asset class for the new asset type.
1. (Optional) Give the asset type a description.
1. (Optional) Specify a three-character prefix to prepend to each asset given this type.
1. (Optional) Toggle the **Auto-generate asset names** switch to on if you want assets  for this type to have names auto-generated based on the asset ID.
1. (Optional) Add an image for the asset type by uploading or dropping a file into the Custom Image box.

### Asset type fields

* **Name.** This is displayed in lists and used for searches and reports. This name is applied to assets created under this asset type.
* **Class.** The asset class you choose determines the asset attributes that are available to the asset type.
* **Description.** Add a few words to help users understand more about the type and how it should be used.
* **Prefix.** This is a three-character prefix that is automatically prepended to the asset ID when you add an asset to the asset type.
* **Auto Generate Name.** When enabled, for any asset that is created under this asset type, the name is automatically created and based on the asset ID. This includes any prefix set.
* **Image.** Add an image as a visual identifier of the asset type. Any asset created using this type will also use this image.

### Deleting an asset type

You can delete an asset type only when there are no assets associated to it.

**To delete an asset type:**

1. In the Asset Categories list, click the row of the asset type you want to remove.
1. Click the **Delete** button (trash can icon). If there are assets associated to the type, you will be prevented from deleting it.
-->