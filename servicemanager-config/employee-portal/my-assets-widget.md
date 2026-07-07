# My Assets Widget

The My Assets widget is an Employee Portal widget that gives users a quick view of assets that they use.

![My Assets Widget](/_books/servicemanager-config/employee-portal/images/my-assets-widget.png)

## Asset visibility criteria

The widget filters assets based on the relationship with the signed-in **Employee Portal** user.

| Relationship | Included? | Definition |
| :--- | :--- | :--- |
| **Used By** | Yes | The asset is assigned to the user as the primary operator. |
| **Shared With** | Yes | The asset is shared with the user or a group the user belongs to. |
| **Owned By** | No | The widget excludes assets if the user is only listed as the owner. |
| **Archived assets** | No | The widget excludes archived assets from the default view. |

## User experience

The widget adapts its interface based on the number of assets associated with the user.

### List management

* **Small asset lists:** If a user has 12 or fewer assets, the widget displays asset cards without search or sort options to maintain a clean interface.
* **Large asset lists:** If a user has more than 12 assets, the widget enables search, ordering options, result counts, and pagination.

### Search and ordering

* **Search:** Available for large lists. The system automatically removes leading and trailing spaces from search queries before processing.
* **Ordering:** Users can sort assets by name, created date, or updated date. The order menu includes arrows for ascending and descending sorts.

### Visual elements

* **Asset links:** Asset names function as links only for users with **Asset Management** view or administration permissions. For all other users, names appear as plain text.
* **Images and icons:** The widget displays uploaded asset images. If no image exists, the widget displays the standard asset class icon.

## Administrator configuration

Administrators use the configuration settings to choose which asset details appear on the cards. These settings only affect the visual presentation and do not change the underlying data scope.

### Ordering details

To change the display order of asset details, drag the options within the configuration panel to the preferred position. The system saves this order as part of the widget configuration.

:::note
These display options are for user convenience and do not function as a security layer for sensitive data.
:::

## Additional data options

Select only the fields that help users identify their assets or complete their tasks. A compact widget works best for homepages, while detailed cards are better for asset-focused pages.

| Option | Field displayed | Recommended use |
| :--- | :--- | :--- |
| **Display asset state** | **State** | Use when users must know if an asset is active. |
| **Display asset substate** | **Substate** | Use for lifecycle or operational context. |
| **Display asset description** | **Description** | Use when the name is insufficient. Note: Long text increases card height. |
| **Display warranty expiry date** | **Warranty expires** | Use for hardware replacement or repair scenarios. |
| **Display asset site** | **Site** | Use for organizations with multiple physical locations. |
| **Display asset location** | **Location** | Use for specific physical assets or shared equipment. |
| **Display assigned user** | **Used by** | Use when ownership and assignment differ. |
| **Display asset owner** | **Owned by** | Use for responsibility or approval contexts. |
| **Display department** | **Department** | Use in department-specific portals. |
| **Display company** | **Company** | Use for multi-company environments. |
| **Display created date** | **Created date** | Use for audit or lifecycle views. |
| **Display last updated date** | **Last updated date** | Use to show how recently information changed. |

## Responsive layout

The widget automatically adjusts the number of columns based on the available screen width to ensure readability.

| Screen size | Layout behavior |
| :--- | :--- |
| **Wide** | Displays the maximum number of configured columns and asset cards per row. |
| **Medium** | Reduces the number of cards per row to maintain clear text and image visibility. |
| **Small** | Stacks asset cards into a single column, allowing users to scroll vertically. |

## Localization and customization strings

Use the following keys in the Service Manager [Translations](/servicemanager-config/customize/service-manager-translations) to customize the text within the widget.

### Widget text strings

| Key | Default value |
| :--- | :--- |
| `employeePortal.widgets.assets.search.placeholder` | Search assets |
| `employeePortal.widgets.assets.search.title` | Search |
| `employeePortal.widgets.assets.search.clear.title` | Clear search |
| `employeePortal.widgets.assets.sort.orderBy` | Order By |
| `employeePortal.widgets.assets.sort.name` | Name |
| `employeePortal.widgets.assets.sort.createdDate` | Created date |
| `employeePortal.widgets.assets.sort.updatedDate` | Updated date |
| `employeePortal.widgets.assets.result.singular` | result |
| `employeePortal.widgets.assets.result.plural` | results |
| `employeePortal.widgets.assets.empty.noAssets` | There are no assets to show for your profile yet. |
| `employeePortal.widgets.assets.error.message` | There is an error with the asset widget. Please contact your Hornbill administrator. |
| `employeePortal.widgets.assets.value.shared` | Shared |

### Configuration strings

| Key | Default value |
| :--- | :--- |
| `employeePortal.widgets.assets.config.name` | My Assets |
| `employeePortal.widgets.assets.config.description` | Assets used or shared with the user |
| `employeePortal.widgets.assets.config.additionalData.label` | Add additional data of assets that you want to show for your users in employee portal: |
| `employeePortal.widgets.assets.config.options.state` | Display asset state |
| `employeePortal.widgets.assets.config.options.warrantyExpires` | Display warranty expiry date |

## Frequently asked questions

|Question|Answer|
|---|---|
|Can administrators choose between Used By, Owned By, or Shared With?|No. The widget always includes **Used By** and **Shared With** assets. It does not include assets where the user is only the owner.|
|Why are search and sort options missing from my list?|If a user has 12 or fewer assets, the toolbar is hidden to keep the interface simple. All assets are visible on the single page.|
|Why does an asset name appear as text instead of a link?|Only users with **Asset Management** view or administration rights can open asset records. Other users see the name as plain text.|
|Why does the card text appear before the asset image?|The widget loads asset data first to ensure the interface is functional. Images load as they become available from the server.|
