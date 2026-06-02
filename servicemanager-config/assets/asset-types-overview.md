---
layout: article-toc
---
# Asset Types Overview

:::note
[[INCLUDE https://raw.githubusercontent.com/Hornbill-Docs/hdoc-library/main/hdoc-library/service-manager/new-assets-note.md]]
:::

Asset management within Hornbill Service Manager allows you to organize and present detailed information about each asset. By organizing assets into specific types, you can establish a comprehensive framework of fields and data tailored to each asset. This approach ensures that all relevant information is readily accessible for any asset.

## Before you begin

* The [Asset Management Admin role](/servicemanager-config/setup/service-manager-roles#asset-management-roles) is required to manage asset types and categories.
* Know how to access the [Service Manager Configuration](/servicemanager-config/index#access-service-manager-configuration).
* Understand how the [asset classes, types, and categories are structured](/servicemanager-config/assets/overview#asset-structure).
* Decide whether you want to [enable asset partitions](/servicemanager-config/assets/manage-partitions) on your instance.

## Accessing asset types

To customize your asset types, navigate to **Configuration > Service Manager > Assets > Manage Types**.

## Manage asset types view

The Manage Types view is broken down into two panels. The left-hand panel shows the list of asset categories and their associated asset types. The right-hand panel shows the details of the selected category or type.

![Manage Asset Types view](/_books/servicemanager-config/images/asset-types-view.png)

### Category and type navigation panel

The left-hand panel allows you to navigate through your asset categories and types. You can expand each category to view the types within it. Selecting a category or type will display its details in the right-hand panel.

#### Partition selection

If you have [asset partitions](/servicemanager-config/assets/manage-partitions) defined, you can select the partition you want to view or manage from the dropdown at the top of the left-hand panel. This allows you to manage asset types specific to that partition.

![Partition selection dropdown](/_books/servicemanager-config/images/asset-types-partition-dropdown.png)

#### Categories and types

[Categories](/servicemanager-config/assets/asset-categories) are displayed in bold, while [types](/servicemanager-config/assets/manage-asset-types) are listed under their respective categories. You can click on any category or type to view and edit its details in the right-hand panel.

![Categories and types list](/_books/servicemanager-config/images/assets-categories-and-types.png)

### Details panel

The right-hand panel displays the details of the selected category or type. Once selected, you can view and edit its name, description, associated fields, and more.
