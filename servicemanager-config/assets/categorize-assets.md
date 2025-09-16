---
title: Organize assets into categories
layout: article
keywords: asset class, asset type
---
# Organize assets into categories

::: note
This article is new, to support the preview release of the new Asset Management and its new UI.
:::

Your asset records are stored under asset types, and your asset types are stored under asset categories. You can create as many categories as you want to meet your organization’s needs. By organizing your assets into categories and then configuring your asset types, you control *how* asset information is displayed and *which* asset information is displayed.

## Before you begin
To access the Asset Management capabilities of Hornbill Service Manager as an admin, your user account must have the following role associated:

|**To do this**|**You need this role assigned**|
|:----|:----|
|Create categories<br>Define and edit asset types<br>Have all the capabilities of the Asset Management User role|Asset Management Admin|

## About categorizing asset types
In setting up your Asset Management implementation, you'll take the following steps:
1. [Determine which asset categories you need to group your asset types.](/servicemanager-config/assets/categorize-assets#determine-your-asset-categories)
1. [Create asset categories.](/servicemanager-config/assets/categorize-assets#create-asset-categories)
1. [Determine your asset types.](/servicemanager-config/assets/categorize-assets#determine-your-asset-types)
1. [Put asset types into categories.](/servicemanager-config/assets/categorize-assets#put-asset-types-into-categories)
1. [Set up details for each category](/servicemanager-config/assets/categorize-assets#set-up-details-for-each-category); customize your presentation of asset information in the list of assets when viewing by category.
1. [Edit asset types to customize the form layout of the asset information.](/servicemanager-config/assets/categorize-assets#edit-the-asset-types)

## Determine your asset categories
Do you have an existing Asset Management implementation in Hornbill? If so, when switching to the new Asset Management, you'll be presented with suggested categories for your assets. To the left, you'll see a list of uncategorized asset types.

**To accept or reject the suggested categories:**
1. Navigate to **Configuration > Service Manager > Assets > Manage Types**.
1. In the main panel to the right, your asset types are shown under suggested categories.
1. Within each suggested category, use the **Select All** and **Select** buttons to choose which of your asset types should go into it.
1. Click **Create and Assign** for each suggested category to accept the suggestions and any changes you made.
1. When you have finished assigning categories in this way, if there remain any uncategorized asset types, [create your own categories](/servicemanager-config/assets/categorize-assets#create-asset-categories)

If you are new to Asset Management in Hornbill and don't have an existing implementation, take some time to consider how you would like to group your asset types and which categories you'll need before moving on to [create them](/servicemanager-config/assets/categorize-assets#create-asset-categories).

## Create asset categories

You can create as many asset categories as you need.

**To create an asset category:**
1. Navigate to **Configuration > Service Manager > Assets > Manage Types**.
1. In the top-right corner of the Asset Categories list, click **Add new category** (the plus sign).
1. In the New Category Details dialog, give the new category a name.
1. (Optional) Enter a brief description of the category.
1. Click **Create**.

## Determine your asset types
If you already have an existing Asset Management implementation in Hornbill, you will already have asset types. You can [create new ones](/servicemanager-config/assets/manage-asset-types#managing-asset-types) in **Configuration > Service Manager > Assets > Manage Types**.

If you are new to Asset Management in Hornbill, you will want to give some thought to the asset types you will need for your implementation. Hornbill provides default asset types for each asset class. You can create as many of your own asset types as you need.

## Put asset types into categories
You can put asset types into categories in the ways that follow. This is done in **Configuration > Service Manager > Assets > Manage Types**.

* **Create new asset types in your categories.** In the Asset Categories list, in the category header, click **Create new type in this category** (the plus sign). For more information, see [Managing asset types](/servicemanager-config/assets/manage-asset-types#managing-asset-types).
* **Drag and drop.** In the Asset Categories list, drag asset types into your categories as appropriate. You can drag an uncategorized asset type into a category, or you can recategorize an asset type by dragging it from one category to another.

### About what's displayed in the assets dashboard
The dashboard is where your organization's Asset Management users can view counts for all your organization’s assets. From each category tile, users can drill down to see the list of assets of that particular asset type. Users can also filter the dashboard view by site and category.

:::tip
Uncategorized assets do not show in the dashboard. Because the assets dashboard is organized by category, if an asset type exists under *Uncategorized*, it will not appear. If you want an asset type to appear in the dashboard, make sure it is in an asset category.
:::

## Set up details for each category
At the category level, you can define your list of available asset table columns. These are the default columns that users see when viewing assets. To show certain columns and hide others, you can limit which fields are available and specify by default which ones are hidden.

To customize how you want the asset information to appear in your asset views, use the *Add* button (e.g. **+ General Field**), which shows additional fields you can add for the current class of assets.

The view below, in **Service Management > Assets**, shows a configuration of asset table columns for an asset category called *Computing devices*. The order of columns has been adjusted, and certain columns (e.g. Description) have been hidden.

![Presentation of asset information in an asset category](/_books/servicemanager-config/assets/images/assets-category-presentation.png)

**To configure the presentation of assets information for an asset category:**
1. In the Asset Categories list, click the header for a category.
1. In the Category Details panel, in Available Asset List Columns, define which columns from the assets table will be available in your list of assets for this asset category.
    * If the asset types in this category use *multiple* asset classes, click **+ General field** to add columns as necessary. If all the asset types in the category use the *same* asset class, then you can use general columns and asset-specific columns. Click **+ General field** and **+*[class name]* field** to add columns as necessary.
       :::note
        You can filter these fields lists, or click **Add All**.
       :::
    * You can choose to use the default columns. If the category includes asset types from multiple asset classes, you can only use general columns.
1. In the list of available columns, click the eye icon to toggle from visible to hidden as necessary.
1. In the list of available columns, drag the column names into the order that you want them to appear.
1. (Optional) To delete columns from the list setup, hover over the column's row and click **Remove field** (the trash can icon).
1. Click **Save Changes**.

## Edit the asset types
This section provides a broad overview of editing asset types. Before configuring your assets types, make sure you understand the more detailed information presented in [Manage assets](/servicemanager-config/assets/manage-asset-types).

1. Set up your form layout for each asset type (you can change it from the default layout).
1. In *Fields to Show in First Column*, drag and drop to change the order of how the information appears in the asset view.
1. Take other actions as necessary, as described in [Managing asset types](/servicemanager-config/assets/manage-asset-types#managing-asset-types). For example, would you like to change from a one-column layout to a two-column layout?
1. (Optional) When you're finished making your modifications, you can [export the whole UI configuration into a JSON file](/servicemanager-config/assets/manage-asset-types#exporting-and-importing-asset-types).

<!----JAMES: Is there anything else we should say here?---->