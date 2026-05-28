---
layout: article-toc
---

# New assets mode infokit

On July 27, 2026, the new asset management functionality will move out of preview and will replace the current asset management which will no longer be available. 

If you currently use asset management in Hornbill, you must audit your current configuration before July 27. This ensures your data migrates correctly and your daily operations continue without interruption. Some configuration tasks are best performed before the switchover occurs.

## Overview of new features

The new asset management mode provides more control over assets through a refreshed interface within the Service Manager application. 
This update includes enhanced layouts, additional classification fields, and the following features:

- **Enhanced layout**. Navigate and manage assets in the Service Manager application more easily with a tabbed interface. 
- **Asset categories**. Use customizable categories to organize and group asset types. These are designed to co-exist with asset classes in the overall asset structure.
- **Auto-save functionality**. Fields save automatically when a value changes. This removes the need for an Edit or Save button.
- **Asset partitioning**. Use partitioning to restrict asset visibility based on the service for both end users and service desk agents.
- **Common custom fields**. Access shared custom fields, including those available in Intelligent Capture form nodes.
- **Bulk actions**. Create or edit multiple assets simultaneously to save time when managing large inventories.
- **View Asset Management application right**. Assign this role to grant read-only access to assets without providing editing privileges.
- **Financial tools** Use the new Assets Under Warranty view and the Asset depreciation calculator.
- **Asset summary card**. View key asset details quickly in a condensed format.

The following video shows how the new Asset Preview can be enabled and highlights some of the new features.

<iframe width="560" height="315" src="https://www.youtube.com/embed/TJWcud1QQXY?si=ad6tDszS7OdBvuUj" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

## Impact on your current configuration

If you are currently using assets, review and complete these tasks before the switchover date:

- **Recreate filters and lists**. Current filters and lists do not migrate to the new mode. Use this transition to evaluate and improve your existing views.
- **Review your asset structure**. In the new mode, there are asset categories available to help organize your assets. The new assets layout in Service Manager displays assets grouped by category. This means that you will need to create your categories and move your asset types into categories. You can also perform additional tasks, such as setting asset summary and detail information.
- **Review your asset types and mandatory fields**. In the new asset mode, mandatory fields you have previously associated with an asset type are not automatically associated. You can migrate your existing fields during creation or rebuild the required fields from scratch using the Quick Layout tool. This is accessed from **Configuration > Service Manager > Manage Types**, then selecting an Asset Type and one of the field types.

Hornbill will be publishing a comprehensive guide to support migrating to the new asset mode that explains these three tasks in more detail.

## Enable the new assets preview

Right now, any user with the Asset Management Admin role can access the new mode from the Service Manager application by selecting **Assets > Switch to new UI**.

Before the mandatory switchover on July 27, 2026, Hornbill Administrators can enable the new interface for specific user groups. This means that they don’t need to switch to the new mode manually and have access to the functionality. This allows your team to transition to the new mode gradually. 

### Before you begin

Ensure you have the Asset Management Admin role.

### Steps

1. Navigate to **Configuration > Service Manager > Application Settings**.
1. Enable the **Include Advanced Settings** checkbox.
1. Locate **guest.app.experimental.enableAssetManagementPreview** in the list. Set this value to true to enable the preview for Asset Managers only. With only this setting enabled, they will be able to revert to the current mode manually.
1. Locate **guest.app.experimental.enableNewAssetManagementUIForAssetUsers** in the list. You can set this value to true to enable the new mode for all asset users. If you choose to enable this setting, asset admins will not be able to manually revert back to the current assets mode from the Service Manager application. To allow that, you must disable this setting.

## Support and guidance

Hornbill is providing several resources to assist with your transition.

### Webinars

- Next-Gen Hornbill Assets: Evolution and capabilities. 6th May: Register to learn about core functionality.
- 8 weeks to go: Your Hornbill Assets readiness walkthrough. 3rd June: Register for a guided preparation session.

### In-person events

Join us at our [Connect Events](https://hornbill.com/events) in June for hands-on activities exploring the new asset mode.

### Documentation

- Migration Guide: A step-by-step guide to support your migration will be published in May 2026.
- [Service Manager Configuration Guide](/servicemanager-config/assets/overview): This guide contains technical details regarding new asset features and functionality.
- Service Manager User Guide: This guide is currently being updated for Asset Managers and general users.
