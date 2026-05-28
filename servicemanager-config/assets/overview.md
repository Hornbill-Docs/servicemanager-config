---
layout: article-toc
---
# Asset management

:::note
[[INCLUDE https://raw.githubusercontent.com/Hornbill-Docs/hdoc-library/main/hdoc-library/service-manager/new-assets-note.md]]
:::

## About asset management

Asset management involves the capturing and detailing of information for the assets within your organization. This includes tracking the ownership, costs, relationships, and life cycle of assets to support strategic decision-making for the IT environment.

Asset management in Hornbill Service Manager gives you the flexibility to configure your implementation to best suit your organization's use case for managing asset records. You can record detailed hardware and software inventory information useful to IT when supporting the users of the assets, and when making decisions about purchases and redistribution.

The assets in Asset management form the foundation of a Configuration Management Database (CMDB). Assets can be used as part of incident, problem, and change processes to assist in incident classification, impact analysis, and change planning.

Asset categories allow you to group your asset types in a customizable way. Users navigate assets by category.

### Where assets are used

* **Intelligent Capture**. When a Service Manager request is being raised, the [Assets Form](/servicemanager-config/customize/service-manager-capture-forms#assets) can be used to select and associate an asset with the newly created request.
* **Workflows**. Use the [Requests Automation for Assets](/servicemanager-config/customize/workflows/requests-automation#assets) to have any asset associated with the customer, linked to the request and automate the updating of these assets.
* **Auto Tasks**.  The [Asset Automation](/servicemanager-config/customize/workflows/asset-automation) can be used to help drive [auto task](/servicemanager-config/customize/service-manager-auto-tasks) workflows on an asset record.
* **Request Asset Action**. Using the [Asset Action](/servicemanager-user-guide/service-portfolio/requests/asset-action), support staff can manually find and link assets that are related to the request.
* **Service Assets**. Add assets that underpin or are supported by a particular [service](/servicemanager-user-guide/service-portfolio/services/service-details).
* **CI Explorer**. Use the [CI Explorer](/configuration-management/configuration-item-explorer) to view a graphical representation of how assets are related to each other, along with other configuration items.

## Roles

The following roles give rights to asset management in Service Manager:

|Role|Description|
|-|-|
|Asset Management User|This role includes rights to define and edit assets as well as to add detailed asset information.|
|Asset Management Admin|This role provides all the capabilities of the Asset Management User role, with additional rights to define and edit asset types and asset categories.|
|Asset Manager|This role should be granted to asset managers for task/activity assignment in Hornbill workflows.|
|Custom Roles|Custom roles can be created and assigned one or more of the following asset management rights: View Asset Management, Create Assets, Edit Assets, Delete Assets, View Asset Audit Trail, Administer Asset Management, View CMS, View Configuration Items, Create Configuration Items, Edit Configuration Items, Delete Configuration Items, viewSoftwareInventory, View Configuration Management.|
