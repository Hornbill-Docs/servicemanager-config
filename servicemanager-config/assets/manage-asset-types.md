---
layout: article-toc
---

# Asset Types

## General

![General tab](/_books/servicemanager-config/assets/images/assets-general-tab.png)

In the General tab, you can set some of the basic information about the asset type and choose an icon or upload a custom image the will be used for all assets of this type.

* **Name**. The name of the asset that will be displayed everywhere assets are used.
* **Category**. The category for this asset type.
* **Description**. A description of this asset type.

### Asset Card customization

The Asset Card is a like a business card that you can design for your asset. Key information of your choice can be added to the card. The defined asset card will appear on all assets defined under this asset type.

Here is an example of a summary card for an asset of the asset type Printer:

![Summary card for an asset](/_books/servicemanager-config/assets/images/assets-summary-card.png)

Where is the asset card displayed?

* When viewing an [asset detail record](/servicemanager-user-guide/asset-management/asset-details).
* When an asset is selected in the [Configuration Item Explorer](/servicemanager-user-guide/configuration-management/configuration-item-explorer).

There are options to customize the Summary Card and the Wide Summary card. The **Summary Card Editor** accepts HTML. Here you can include the values held in class custom fields. The syntax for this is:

* For common custom fields use `{{general.h_custom_char1}}`, replacing `char1` with the term in the custom field.
* For class specific fields use `{{extended.h_custom_ext_char1}}`, replacing `char1` with the term in the custom field.

To help you add the correct fields, a dropdown menu appears as you type the variable name in the editor, as this screenshot shows:

![Asset Summary Card editor dropdown](/_books/servicemanager-config/assets/images/asset-field-dropdown.png)

You can test how summary cards will be presented by selecting specific assets to preview in the summary card editor.

::: warning
When using the Summary Card Editor to customize asset summary cards, use *only* Hornbill-prescribed styles. Do not add your own styles; any other style declarations will be removed by Hornbill.
:::

## Summary fields

![Summary Fields tab](/_books/servicemanager-config/assets/images/assets-summary-fields-tab.png)

Go to the Summary Fields tab to choose the fields that a user sees when viewing an asset in the Summary view. The focus of an asset is put on this summary information when a user clicks on an asset in the asset list. You can customize the list of Summary fields so as to highlight the most important or most used fields for this type of asset.

Choose between a one-column or two-column layout of the fields. Use the **Quick Layout** button to choose to use default fields or legacy fields. Using legacy fields means Hornbill will read in your asset fields from your existing implementation.

Here is an example of a Summary view for an asset of the asset type Printer, using a one-column layout:

![Fields in an asset's Summary view](/_books/servicemanager-config/assets/images/summary-view-of-asset.png)

Here is the Summary view of the same asset, with fields configured in a two-column layout:
![Fields in an asset's Summary view, two-column layout](/_books/servicemanager-config/assets/images/summary-view-of-asset-2-column.png)

## Detail fields

![Detail Fields tab](/_books/servicemanager-config/assets/images/assets-detail-fields-tab.png)

In the Details view, users can access extended details beyond what is in the Summary view for an asset. Go to the Detail Fields tab to choose which fields you want users to see when viewing an asset in the Details view.

Choose between a one-column or two-column layout of the fields. Use the **Quick Layout** button to choose to use default fields or legacy fields. Using legacy fields means Hornbill will read in your asset fields from your existing implementation.

## Create fields

![Create Fields tab](/_books/servicemanager-config/assets/images/assets-create-fields-tab.png)

Go here to choose the fields available to a user when creating new assets. Use the **Quick Layout** button to choose to use default fields or legacy fields. Using legacy fields means Hornbill will read in your asset fields from your existing implementation.

Here is an example of a New Asset dialog when creating an asset of the asset type Printer:

![New Asset dialog](/_books/servicemanager-config/assets/images/create-new-asset.png)

## List fields

![List Fields tab](/_books/servicemanager-config/assets/images/assets-list-fields-tab.png)

Go to the List Fields tab to choose the fields that a user sees when viewing the list of assets in an asset type. You can drag the columns to change the order in which they appear in the list. Click the eye icon to toggle the columns from visible to hidden.

Here is an example of a what a users sees when viewing the list of assets by the asset type Printer:

![List view when viewing by asset type](/_books/servicemanager-config/assets/images/list-view-for-asset-type.png)

**Fields available for searching.** As an admin, you can configure the fields that are available for searching. If you want your users to be able to search for assets using specific fields, then add those fields here in the List Fields tab by adding additional columns. Once a column is added, it is available in the search.

**Fields available for CSV download.** The CSV download contains only the columns that you have added here in the List Fields tab.

## Archiving asset types and assets

Archiving helps you manage your asset library by restricting access to older items and preventing the creation of new assets in archived types.

When you archive an item, the system does not delete any data. Instead, it changes the state of the assets to archived.

 When you archive assets, you can select specific asset state groups and sub states to include. The system does not affect any groups you do not select.

To archive asset types and their associated assets, select the archive button that appears when an asset type is selected in the left-hand menu, as highlighted here:

![asset type archive button](/_books/servicemanager-config/assets/images/asset-type-archive.png)

When an asset type is archived, this becomes the unarchive button.

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

### Unarchive an asset type

1. Select the archived item in the navigation tree.
2. Select the **Unarchive** button.
3. Choose the unarchive mode that matches your needs (such as **Type only** or **Type & assets**).
4. If you unarchive assets, review the groups organized by their current sub state.
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
