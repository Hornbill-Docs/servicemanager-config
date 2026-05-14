---
layout: article
keywords: common fields
---
# How assets are structured

:::note
[[INCLUDE https://raw.githubusercontent.com/Hornbill-Docs/hdoc-library/main/hdoc-library/service-manager/new-assets-note.md]]
:::

With Asset Management in Hornbill Service Manager, every asset is part of an asset type, and those asset types are organized into asset categories. In the data tables behind the scenes, each asset type is part of an asset class. Asset category names can resemble class names. But, when setting up the management of your assets, it's the asset categories --- and the ability to create your own categories --- that give you the flexibility to create what's best for your organization's needs.

![Asset Structure](/_books/servicemanager-config/assets/images/asset-structure.png)

## Asset classes

Asset classes are predefined and fixed. You cannot modify asset classes. Think of asset classes as templates that provide the data fields for IT assets. Each asset class has a set of available attributes that can be hidden or made available to each of the various asset types you create. By hiding attributes you don't need, you ensure that only the relevant information is visible in your asset records.

When creating a new asset type, you must choose a class. This is because the class chosen dictates which attributes (data fields from the template) are available to populate when adding your individual assets beneath an asset type.

Hornbill's asset classes are the following:

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

:::tip
To view each asset class's attributes and other information (e.g. for use when importing asset data), click the links above to go to the relevant pages in the [Service Manager Database Schema Reference](/servicemanager-external-db/welcome).
:::

### Attributes available to all assets

In addition to the data fields specific to the classes listed above, there are fields shared between all assets, regardless of asset class. These *common fields* are documented in the  in the [Service Manager Database Schema Reference](/servicemanager-external-db/tables/h-cmdb-assets).

## Asset types

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
