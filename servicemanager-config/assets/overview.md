---
layout: article-toc
---
# Asset management

:::note
[[INCLUDE https://raw.githubusercontent.com/Hornbill-Docs/hdoc-library/main/hdoc-library/service-manager/new-assets-note.md]]
:::

## Introduction to asset management

Asset management allows you to capture and detail information for the assets in your organization. You can track ownership, costs, relationships, and the life cycle of assets to support strategic decisions for your IT environment.

In Hornbill Service Manager, you can configure your implementation to suit your specific needs. You can record hardware and software inventory information to help IT support users and make decisions about purchases or redistribution.

Assets in Service Manager form the foundation of a Configuration Management Database (CMDB). You can use asset records in incident, problem, and change processes to assist with classification, impact analysis, and change planning.

Asset categories allow you to group your asset types. Users navigate and find assets based on these categories.

### Asset integration points

You can use assets across several areas of Service Manager:

* **Intelligent Capture**: Use the [Assets form](/servicemanager-config/customize/service-manager-capture-forms#assets) to select and associate an asset with a new request.
* **Workflows**: Use [Requests Automation for Assets](/servicemanager-config/customize/workflows/requests-automation#assets) to link assets associated with a customer to a request. This also automates asset record updates.
* **Auto tasks**: Use [Asset Automation](/servicemanager-config/customize/workflows/asset-automation) to trigger [auto task](/servicemanager-config/customize/service-manager-auto-tasks) workflows on an asset record.
* **Request asset action**: Use the [Asset Action](/servicemanager-user-guide/service-portfolio/requests/asset-action) menu to find and link assets to a request manually.
* **Service assets**: Add assets that support or underpin a specific [service](/servicemanager-user-guide/service-portfolio/services/service-details).
* **CI Explorer**: Use the [CI Explorer](/configuration-management/configuration-item-explorer) to view a diagram of how assets relate to each other and other configuration items.

## Asset management roles

The following roles provide specific rights for managing assets in Service Manager:

| Role | Description |
| :--- | :--- |
| Asset Management User | Provides rights to define and edit assets and add detailed asset information. |
| Asset Management Admin | Provides all rights of the Asset Management User role, plus rights to define and edit asset types and categories. |
| Asset Manager | Assign this role to users who manage tasks and activities within Hornbill workflows. |
| Custom Roles | You can [create custom roles](/servicemanager-config/setup/service-manager-roles#user-created-roles) with specific permissions, such as View Asset Management, Create Assets, Edit Assets, Delete Assets, View Asset Audit Trail, and Administer Asset Management. |

## Asset structure

In Hornbill Service Manager, every asset belongs to an asset type. You organize these asset types into asset categories.

In the backend database, every asset type belongs to an asset class.

![Asset Structure](/_books/servicemanager-config/images/asset-structure.png)

## Asset classes

Asset classes are predefined and fixed. You cannot modify them. Asset classes act as templates that provide the data fields for your assets.

Each asset class contains a set of attributes. You can hide or show these attributes for each asset type you create. By hiding unnecessary attributes, you ensure that asset records only display relevant information.

When you create a new asset type, you must select a class. The class determines which data fields are available for the assets under that type.

Hornbill includes the following asset classes:

* [Computer System](/servicemanager-external-db/tables/h-cmdb-assets-computer)
* [Computer Peripheral](/servicemanager-external-db/tables/h-cmdb-assets-computer-peripheral)
* [Data Processing Record](/servicemanager-external-db/tables/h-cmdb-assets-data-processing-record)
* [General](/servicemanager-external-db/tables/h-cmdb-assets-basic)
* [Mobile Device](/servicemanager-external-db/tables/h-cmdb-assets-mobile-device)
* [Network Circuit](/servicemanager-external-db/tables/h-cmdb-assets-network-circuit)
* [Network Device](/servicemanager-external-db/tables/h-cmdb-assets-network-device)
* [Printer](/servicemanager-external-db/tables/h-cmdb-assets-printer)
* [Software](/servicemanager-external-db/tables/h-cmdb-assets-software)
* [System](/servicemanager-external-db/tables/h-cmdb-assets-system)
* [Telecoms](/servicemanager-external-db/tables/h-cmdb-assets-telecoms)

## Asset types

Service Manager includes several default [asset types](/servicemanager-config/assets/manage-asset-types) to help you start adding assets immediately. Users select an asset type when they add an asset manually. Administrators can specify asset types during data imports and can edit or delete default types.

Default asset types include:

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
