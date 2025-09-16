---
layout: article-toc
---

# Manage asset types

::: note
This article is new, to support the preview release of the new Asset Management and its new UI. You can find documentation for the legacy UI [here](/servicemanager-user-guide/asset-management/manage-asset-types).
:::

Asset Management in Hornbill Service Manager gives you the control to organize and present specific information front and center in the main view of an asset. On a type-by-type basis, you can customize users' view of asset information precisely as you need to.

## Topics covered
* [About configuring asset types](/servicemanager-config/assets/manage-asset-types#about-configuring-asset-types)
* [Managing asset types](/servicemanager-config/assets/manage-asset-types#managing-asset-types)
* [Managing asset states and substates](/servicemanager-config/assets/manage-asset-types#managing-asset-states-and-substates)

## About configuring asset types
To customize your users' view of assets, navigate to **Configuration > Service Manager > Assets > Manage Types**. Here you'll work in the following tabs:
* [General](/servicemanager-config/assets/manage-asset-types#general). Configure the asset type's summary card, its icon, and so on.
* [Summary fields](/servicemanager-config/assets/manage-asset-types#summary-fields). Choose the fields that a user sees when viewing an asset in the Summary view.
* [Detail fields](/servicemanager-config/assets/manage-asset-types#detail-fields). Choose the fields that a user sees when viewing an asset in the Details view.
* [Create fields](/servicemanager-config/assets/manage-asset-types#create-fields). Choose the fields available to users when new assets are being created.
* [List fields](/servicemanager-config/assets/manage-asset-types#list-fields). Choose the fields that a user sees when viewing the list of assets in an asset type.

::: tip
You may find it helpful, when customizing your asset views, to work with two windows open side by side, with one window showing Service Manager > Assets > [a selected asset] and the second window showing your configuration work in **Configuration > Service Manager > Manage Types > [a selected type]**. This way, you can see your modifications in real time.
:::

### General
![General tab](/_books/servicemanager-config/assets/images/assets-general-tab.png)

In the General tab, you can choose an icon for the asset type or upload a custom image.

Go here to configure the summary card that appears for all assets within the asset type. Here is an example of a summary card for an asset of the asset type Printer:

![Summary card for an asset](/_books/servicemanager-config/assets/images/assets-summary-card.png)

::: warning
When using the Summary Card Editor to customize asset summary cards, use *only* Hornbill-prescribed styles. Do not add your own styles; any other style declarations will be removed by Hornbill.
:::

In the General tab, you can also use the dropdown to change the category of the asset type (rather than dragging/dropping).

The General tab is also where you can [export and import your Assets UI configuration](/servicemanager-config/assets/manage-asset-types#exporting-and-importing-asset-types).

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

![List view when viewing by asset type](/_books/servicemanager-config/assets/images/list-view-for-asset-type.png)<br><br>

<!-- ----JAMES: in this post https://beta.hornbill.com/hornbill/post/urn:buzz:activity:d235058b-5d34-4d6f-8dd9-1ce5b47f281c/ you mentioned responding to a customer about limited search functionality. "We need to search for assets using specific fields based on certain criteria. However, the available search filters are limited and do not include all the necessary fields, as shown in the attached image." Would it be worth adding a tip here, like the one below? (I added two H4 sections based off your response to the customer's post.) -->

**Fields available for searching.** As an admin, you can configure the fields that are available for searching. If you want your users to be able to search for assets using specific fields, then add those fields here in the List Fields tab by adding additional columns. Once a column is added, it is available in the search.

**Fields available for CSV download.** The CSV download contains only the columns that you have added here in the List Fields tab.

## Managing asset types
Service Manager provides a number of asset types by default so that you can quickly start adding your assets. Users can select an asset type when manually adding an individual asset. Admins can specify asset types as part of an import. Admins can also edit or delete the default asset types as necessary.

The default asset types include the following:
* Desktop
* Laptop
* Server
* Virtual machine
* Headset
* Keyboard
* Monitor
* Mouse
* Webcam
* Smartphone
* Tablet
* Printer
* Scanner
* Desktop app
* Mobile app
* Desk phone

For details about choices to make when creating a new asset type, see [Asset type fields](/servicemanager-config/assets/manage-asset-types#asset-type-fields).

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

### Exporting and importing asset types
During the implementation phase of your Service Manager deployment, you may want to export asset types for a later import on the same Hornbill instance or another one -- for example, to back up and restore your asset type configuration. You can export the layout of an asset type to a JSON file, (even make changes if necessary), then import the file. You must import the configuration to the same asset type it was exported from.

**To export an asset type:**
1. Navigate to **Configuration > Service Manager > Assets > Manage Types**.
1. In the Asset Categories panel, select the asset type you want to export.
1. In the General tab, click the ellipsis button and select **Export**.
1. (Optional) Make changes to the JSON file as necessary.
1. (Optional) When you are ready to import the JSON file, follow the steps above and from the ellipsis, select **Import**.

## Managing asset states and substates
Asset states tell you where an asset is in its lifecycle (e.g., *Current*, *Active*, *Archived*). With substates, you can add a customizable layer of detail within those states, allowing you to reflect more specific conditions or workflows.

For example:
* State: Current → Substate: In Stock (for assets awaiting allocation).
* State: Active → Substate: Allocated (for assets assigned to users).

The purpose of substates is to enhance tracking, searching, and reporting by providing more granularity, making it easier to manage assets based on their exact condition or stage.

Substates are global, so you can define them for each state across all asset types.

While asset states are fixed, asset substates are not fixed; you can create new substates under asset states as needed. You control the visibility of both asset states and asset substates for each asset type. You also control whether the state and substate fields are mandatory and read-only.

**To add an asset substate:**
1. Navigate to **Configuration > Service Manager > Assets > Manage Substates**.
1. In the list of states (Current, Active, Archived), in the row of the state for which you want to create a substate, click **Create** (the plus sign).
1. In the Create Substate dialog, give your new substate a name and click **Create**.

**To make an asset state or substate visible or hidden:**
1. Navigate to **Configuration > Service Manager > Assets > Manage Types**.
1. In Asset Categories, select an asset type for which you have added asset states or substates.
1. Click the List Fields tab.
1. In the Available Asset List Columns, for the state or substate you want to control visibility, toggle the eye icon ON or OFF.

**To make an asset state or substate mandatory and/or read-only:**
1. Navigate to **Configuration > Service Manager > Assets > Manage Types**.
1. In Asset Categories, select an asset type for which you have added asset states or substates.
1. Click the Detail Fields tab.
1. In the list of fields, in the row of the state or substate field, click **Field Properties** (the cog icon).
1. In the State dialog, in the *Read-only* dropdown, select Yes or No.
1. In the State dialog, in the *Mandatory* dropdown, select Yes or No.
1. Click **Save Changes**.

<!-- https://wiki.hornbill.com/index.php?title=Asset_Types -->