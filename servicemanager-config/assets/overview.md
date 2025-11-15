---
layout: article-toc
---
# Asset management

::: note
This documentation covers the preview release of the new Asset Management features and user interface. You can find documentation for the legacy UI [here](/servicemanager-user-guide/asset-management/overview-legacy-doc).
:::

## New Asset Preview
The following video shows how the new Asset Preview can be enabled and highlights some of the new features.

<iframe width="560" height="315" src="https://www.youtube.com/embed/TJWcud1QQXY?si=ad6tDszS7OdBvuUj" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

### Preview visibility
Any user who has the Asset Manager role will see the option `Switch to New UI` when the Assets option under the Service Manager menu has been selected. When an Asset Manager switches to the new UI, only they will see the new UI.  Other users with the Asset Manager role can individually switch to the new UI.

![Turn on Asset Preview](/_books/servicemanager-config/images/turn-on-asset-preview.png)

Asset Users will not see the new UI by default.  When you are ready to share the new UI with asset users, the [Service Manager application setting](/servicemanager-config/advanced-tools-and-settings/application-settings) `guest.app.experimental.enableNewAssetManagementUIForAssetUsers` can be turned on to give them access.

## About asset management
Asset management involves the capturing and detailing of information for the assets within your organization. This includes tracking the ownership, costs, relationships, and life cycle of assets to support strategic decision-making for the IT environment.

Asset management in Hornbill Service Manager gives you the flexibility to configure your implementation to best suit your organization's use case for managing asset records. You can record detailed hardware and software inventory information useful to IT when supporting the users of the assets, and when making decisions about purchases and redistribution.

The assets in Asset management form the foundation of a Configuration Management Database (CMDB). Assets can be used as part of incident, problem, and change processes to assist in incident classification, impact analysis, and change planning.

Asset categories allow you to group your asset types in a customizable way. Users navigate assets by category.

#### Where assets are used
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