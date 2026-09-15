---
draft: true
---

# Asset global search settings

Administrators can configure the Assets search in the top navigation bar to target specific fields and include asset tags or archived assets. These global settings establish the default behavior for all users, though users can override these defaults for individual searches using advanced search options.

![Global Search](/_books/servicemanager-config/assets/images/asset-global-search.png)

## Before you begin

* The **Asset Management Admin** role is required to configure global search settings.
* Know how to access the [Service Manager Configuration](/servicemanager-config/index#access-service-manager-configuration).
* Understand how [asset classes, types, and categories are structured](/servicemanager-config/assets/overview#asset-structure).

## Access global search settings

1. Open **Configuration**.
2. Navigate to **Service Manager** > **Assets** > **Global Search Settings**.

## Configure search options

The **Search options** section determines the default scope of the search. Both options are disabled by default.

![Global Search Options](/_books/servicemanager-config/assets/images/asset-global-search-options.png)

1. Select **Also search asset tags** to match search terms against the names of tags attached to assets.
2. Select **Also search archived assets** to include archived assets and assets belonging to archived types in search results.

## Manage fields to search

The **Fields to search** section defines which specific asset record fields the system matches against a search term. The system saves changes to this list automatically.

![Global Search Fields](/_books/servicemanager-config/assets/images/asset-global-search-fields.png)

### Add a field

1. Select **Add field**.
2. From the list of available text-based fields, select the checkboxes for the fields you want to include.
3. Select **Add**.

> **Note:** The system only supports text-based fields (such as identifiers, names, and descriptions) for global search. It excludes numeric or coded fields like operational state.

### Remove a field

1. Locate the field in the list.
2. Select the **Bin** icon next to the field name.

### Field constraints and defaults

* **Field limit:** You can add a maximum of 10 fields. The current count appears next to the section heading (for example, `7/10`). You must remove a field before adding another if you reach the limit.
* **Revert to Default:** Select this option to restore the default field list and disable both search options.

The default configuration includes the following fields:

* **Asset ID**
* **Name**
* **Description**
* **Class**
* **Owned by**
* **Used by**
* **Asset Tag**

## How users search for assets

Users search for assets from the search box in the top navigation bar, the same way as any other global search. Typing a term and searching matches it against every field an administrator has added to **Fields to search**.

### Advanced search options

Below the search box, two dropdowns let a user override the administrator's defaults for a single search. Both dropdowns already show the current default, so a search behaves exactly as configured unless a user changes one.

| Option | Values | Effect |
| :--- | :--- | :--- |
| **Search by Tags** | Include Tags / Exclude Tags | Whether this search also matches against asset tags |
| **Search Archived Assets** | Include Archived Assets / Exclude Archived Assets | Whether this search also matches archived assets |

### Reading search results

Above the results list, selecting the information icon next to the result count opens a panel showing exactly what the search matched against: the fields searched, and whether tags and archived assets were included. This is the first place to check when an expected asset doesn't appear in results.

![Global Search Results](/_books/servicemanager-config/assets/images/asset-global-search-results.png)

## Related settings reference

| Setting | Default |
| :--- | :--- |
| Fields searched | Asset ID, Name, Description, Class, Owned by, Used by, Asset Tag |
| Also search asset tags | Off |
| Also search archived assets | Off |
| Maximum fields | 10 |
