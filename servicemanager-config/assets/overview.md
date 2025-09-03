---
layout: article-toc
---
# Asset management

::: note
This article is new, to support the preview release of the new Asset Management and its new UI. You can find documentation for the legacy UI [here](/servicemanager-user-guide/asset-management/overview-legacy-doc).
:::

Asset management involves the capturing and detailing of information for the assets within your organization. This includes tracking the ownership, costs, relationships, and life cycle of assets to support strategic decision-making for the IT environment.

Asset Management in Hornbill Service Manager gives you the flexibility to configure your implementation to best suit your organization's use case for managing asset records. You can record detailed hardware and software inventory information useful to IT when supporting the users of the assets, and when making decisions about purchases and redistribution.

<!--For each asset type that you create, you can customize all the data that is shown in the details and also in the table list. So when you look at the list of assets for any given type, if it's just that type you'll get obviously all the common asset fields plus the extended asset fields. You can create any number of categories. You can customize the categories of what you see in your asset lists for each category, and if a category has multiple types of the same class, then that Categories list can also include the class-specific columns. So you've got a lot of control over how the data is represented, and then on an asset-type by asset-type basis, you can fully customize the Details view all of the data that's being shown for that type, and you've got control over every aspect of it.-->

The assets in Asset Management form the foundation of a Configuration Management Database (CMDB). Assets can be used as part of Incident, Problem, and Change processes to assist in incident classification, impact analysis, and change planning.

Asset categories allow you to group your asset types in a customizable way. Users navigate assets by category.

## Before you begin
To access the Asset Management capabilities of Hornbill Service Manager, your user account must have one of the following roles associated:

|Role|Description|
|-|-|
|Asset Management User|This role includes rights to define  and edit assets as well as to add detailed asset information.|
|Asset Management Admin|This role provides all the capabilities of the Asset Management User role, with additional rights to define and edit asset types and asset categories.|

## Customizing your implementation of Asset Management
As an Asset Management admin, you'll take the following steps to set up your implementation. First, make sure you [understand the structure of assets](/servicemanager-config/assets/asset-structure) so you can plan how to best meet your organization's needs.

**In setting up your Asset Management implementation, you'll take the following steps:**
1. Determine which asset categories you need to group your asset types.
1. Create the categories.
1. Determine your asset types. Which of the default types will you use? Which new types of your own will you add?
1. Drag and drop asset types into your categories. You can drag an uncategorized asset type into a category, or you can drag an asset type from one category to another (to recategorize it).
1. Create new asset types in your categories.
1. Set up details for each category; customize how you want the asset information to appear in the asset views.
1. Edit asset types to customize how the information appears in the asset views.

*where does import fall?*
<!--
____
Views and advanced filters are the same as before.

## Features
* **Manage Assets.** Access to your organization's assets
* **Manage Asset Types.** Define the types of assets that are used by your organization. Control the available fields and information used on each asset type.
* **Upload Assets.** For small batch imports of assets, use our simple CSV import.
* **Asset Tags.** Create and managed tags that can be used on individual assets. This includes an option to enable or disable the ability for a user to add their own tags, or force them to use a defined set of tags.

## Integration
If you already have an asset-discovery tool or a second asset database, you can set up automated imports and updates using the [Hornbill Asset Import utility](/data-imports-guide/assets/overview). This utility lets you connect to a local database within your network and push the information up to your Hornbill instance.
____
-->
<!--
Database Asset Import

:::note
If Assets are added using data::entityAddRecord API, the Asset URN must be set against each individual Asset record. This can be achieved using data::entityUpdateRecord API. Please remember to replace [Asset Id] with the generated value in h_pk_asset_id column in h_cmdb_assets table.

 <params>
   <application>com.hornbill.servicemanager</application>
   <entity>Asset</entity>
   <primaryEntityData>
     <record>
       <h_pk_asset_id>[Asset Id]</h_pk_asset_id>
       <h_asset_urn>urn:sys:entity:com.hornbill.servicemanager:Asset:" + [Asset Id]</h_asset_urn>
     </record>
   </primaryEntityData>
 </params>

 :::
 -->