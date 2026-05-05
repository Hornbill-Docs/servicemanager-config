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

Archiving allows you to restrict access to assets and prevent new assets being created in archived categories and types. 

With asset archiving, nothing is permanently deleted.

Asset archiving is simply changing the state of assets to archived. When archiving from the Manage Types page, you can select the asset state groups, including sub states, to include in the archive. Unselected groups will not be affected.

You can archive asset categories, types, and their associated assets by selecting the archive button that appears when a category or type is selected in the left-hand menu, as highlighted here:

![asset type archive button](/_books/servicemanager-config/assets/images/asset-type-archive.png)

With archiving:

* Archiving an asset type opens a dialog. Select an archive mode (type only, or type & assets) and, in assets mode, selects which asset state groups to archive and optionally assigns a sub state to each.
* Archiving a category opens a dialog. Select an archive mode (category only, category & types, or category/types/assets). In assets mode a per-type per-state breakdown is shown with sub state selection per row.
* Unarchiving an asset type opens a matching popup. The user chooses unarchive mode (type only, or type & assets). In assets mode, archived asset groups are shown grouped by current sub state, and the user picks a new state and optional new sub state for each selected group.
* Unarchiving a category opens a popup with three modes mirroring the archive flow. In assets mode, only archived types and their archived asset groups are shown; the user assigns a new state and optional new sub state per group.
* Archived categories and types are displayed in italic text in the nav tree. When not currently selected they are also muted; when selected the muting is suppressed so the active item remains readable.
* From **Service Manager** > **Assets**, users with asset management rights can toggle visibility of archived items via the eye icon button in the **Assets** title bar. The icon is open when archived items are shown and closed  when hidden, giving an at-a-glance indicator of the current setting. This preference is saved per user via the app setting assets.view.showArchived.
* From **Service Manager** > **Assets**, users without any asset management rights cannot see archived categories or types in the nav tree at all. This is enforced by the tree component independently of the user preference setting.
* Editing of archived records is fully permitted — there are no form-level restrictions.
* Archived asset types are excluded from the type dropdown in the Create Asset popup, preventing new assets from being created against an archived type.

### Auditing archive events

Asset archiving can also be performed in Service Manager. This is done by updating the asset state in the asset editor and be done for one or multiple assets at a time.

When archiving assets in Service Manager you have the option to audit the update. Auditing asset type archiving or asset archiving is not possible when archiving from the Manage Types page.

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