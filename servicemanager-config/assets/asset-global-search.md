---
draft: true
---

# Asset Global Search

The Assets search in the top navigation bar can be configured to search a set of fields you choose, rather than a fixed list, and can optionally match against asset tags and archived assets. Search behavior is set globally by an administrator, and can be overridden by users for a single search using the advanced search options.

![Global Search](/_books/servicemanager-config/assets/images/asset-global-search.png)

## Before you begin

* The **Asset Management Admin** role is required to configure global search settings.
* Know how to access the [Service Manager Configuration](/servicemanager-config/index#access-service-manager-configuration).
* Understand how [asset classes, types, and categories are structured](/servicemanager-config/assets/overview#asset-structure) — only fields on the base asset record can be added to the search.

## Accessing global search settings

To configure which fields and asset states the Assets search uses, navigate to **Configuration > Service Manager > Assets > Global Search Settings**.

## Global search settings view

The Global Search Settings view is broken down into two sections. The **Search options** section controls whether tags and archived assets are matched by default. The **Fields to search** section controls which asset fields are matched.

Changes in both sections save automatically — there is no separate save action.

![Global Search Settings](/_books/servicemanager-config/assets/images/asset-global-search-settings.png)

### Search options

* **Also search asset tags:** When enabled, a search also matches against the names of tags attached to an asset, not just its own fields.
* **Also search archived assets:** When enabled, archived assets — and assets of an archived type — are included in search results. When disabled, they're excluded by default.

Both options are off by default.

### Fields to search

The field list shows every field currently included in the search, in a table with a remove control alongside each one.

* **Add field:** Opens a list of the fields available to add, drawn from the base asset record. Only fields suited to free-text search are offered — identifiers, names, descriptions, and similar text fields — not coded or numeric fields such as operational state. Tick any number of fields and select **Add** to confirm.
![Global Search Add Field](/_books/servicemanager-config/assets/images/asset-global-search-add-field.png)
* **Remove a field:** Select the bin icon next to a field in the list.
* **Field limit:** The list accepts a maximum of **10 fields**, shown as a count next to the section heading (for example, `7/10`). Remove a field before adding another once the limit is reached.
* **Revert to Default:** Restores the built-in default field list and switches both search options off.

::: note
The built-in default searches **Asset ID**, **Name**, **Description**, **Class**, **Owned by**, **Used by**, and **Asset Tag**, with both search options off.
:::

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
