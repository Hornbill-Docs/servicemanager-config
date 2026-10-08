---
layout: article-toc
---

# Common Asset Actions

Asset Actions are configurable buttons that appear on asset records. When selected, an action can open a URL in a popup or in a new browser tab, or trigger an [Auto Task](/servicemanager-config/customize/service-manager-auto-tasks), all within the context of the asset being viewed.

Common Asset Actions is a collection of asset actions that are available to the selected partition. Rather than creating an asset action for each asset type, you can create a single asset action and link it to multiple asset types.

> **Note:** Asset actions replace the existing [asset custom buttons](/servicemanager-user-guide/asset-management/asset-details#custom-buttons), providing a more centralized configuration that makes use of asset partitions.

## Before you begin

* The [Asset Management Admin](/servicemanager-config/setup/service-manager-roles#asset-management-roles) role is required to configure Asset Actions.
* Know how to access the [Service Manager Configuration](/servicemanager-config/index#access-service-manager-configuration).
* Understand how [asset partitions](/servicemanager-config/assets/manage-partitions) and [asset types](/servicemanager-config/assets/manage-asset-types) are structured.
* Read about adding Asset Actions to [individual asset types](/servicemanager-config/assets/manage-asset-types#actions).

## Enabling Asset Actions

Asset Actions must be enabled separately for each partition. Until enabled, the feature is inactive and [Custom Buttons](/servicemanager-user-guide/asset-management/asset-details#custom-buttons) continue to appear for assets in that partition.

![Enable Asset Actions](/_books/servicemanager-config/assets/images/asset-actions-enable.png)

1. Navigate to **Configuration > Service Manager > Assets > Manage Types**.
1. Select the partition you want to enable Asset Actions for.
1. Below the partition name, select **Common Asset Actions**. If the feature has not yet been enabled for this partition, the feature overview panel is shown.
1. Choose how you want to start, then select **Enable Asset Actions**:
    * **Enable only**: Enables the feature with an empty action list. You build your actions from scratch.
    * **Enable and Import from Custom Buttons**: Enables the feature and immediately imports your existing Custom Buttons as Asset Actions. See [Importing from Custom Buttons](#importing-from-custom-buttons) for details of how the import works.
    * **Enable and Import from Partition**: Enables the feature and copies all partition-scoped and class-scoped actions from another partition into this one. Select the source partition from the dropdown. Only partitions that already have actions are shown.

Once enabled for a partition, Asset Actions are rendered in place of Custom Buttons on asset records within that partition. Custom Buttons are not deleted. They remain in the Custom Buttons configuration, but they no longer appear while Asset Actions is active.

## Creating a common action

Start by selecting the partition where you want to create the action. Below the partition name, select **Common Asset Actions**.

1. In the Common Asset Actions panel, select **+ Add Action**.
1. The details form opens. Set the [scope](#scope), then fill in the [display](#display) fields, [action](#action) type settings, and [options](#options).
1. Select **Save**. The action is created and appears in the list.

> **Note**: After saving, an action does not appear on any asset records until it is [linked](#linking-actions-to-asset-types) to one or more asset types.

### Scope

The scope determines where the action can be used. The scope can only be set when the **Asset Action** is being created and cannot be changed afterwards.

* **Partition**: These actions belong to the entire partition and can be linked to any asset type within it, regardless of class. Use this scope for actions that should be available across many or all asset types in the partition.

* **Class**: These actions belong to a specific class within the partition. They can only be linked to asset types of that class within the partition. Use this scope when an action only makes sense for a particular class of asset.

> **Note**: Asset actions can also be created on an individual [asset type](/servicemanager-config/assets/manage-asset-types#actions). These are not shared and can't be linked to any other asset type.

### Display

| Field | Description |
| :--- | :--- |
| Label | The text shown on the button or in the dropdown list. Required unless an icon is set. |
| Description | Text shown when a user hovers over the button. Optional but recommended for less obvious actions. |
| Button Style | The color style for the button: Default (gray), Primary (blue), Success (green), Danger (red), Warning (yellow), Info (light blue). |
| Icon | An icon displayed alongside the button label, chosen using the icon picker. Optional. |

### Action

#### URL

Opens a URL in a new browser tab. The URL can contain `{{fieldName}}` variable tokens. Use this to link to an external system, a deep link elsewhere in the platform, or any web address relevant to the asset.

If the URL does not include a protocol (`://`), `http://` is automatically prepended at runtime.

**Required:** URL field.

The optional **Activity Message** field (under Options) allows a note to be written to the asset's activity stream each time this action is triggered. The message supports variable tokens and is written after the URL is opened.

#### Auto Task

Triggers an Auto Task when the user selects the button. The asset's URN is automatically passed as the `objectRefUrn` input parameter so the Auto Task knows which asset it is operating on.

| Setting | Description |
| :--- | :--- |
| Auto Task Name *(required)* | The exact name of the Auto Task process to trigger. Select from the dropdown list of available processes. |
| Open popup with Auto Task progress | Shows a modal window that tracks the Auto Task as it runs, matching the progress view shown by the existing Custom Buttons feature. |
| Display Auto Task progress in timeline | Posts a link to the started Auto Task in the asset's activity stream, giving a record of when the action was triggered. |
| Prompt for confirmation before running | Shows a confirmation prompt before the Auto Task starts. You can customize the prompt text (for example, *"Are you sure you want to retire this asset?"*). |
| Additional input parameters | A table of extra key/value pairs passed as BPM input parameters alongside the standard asset fields. Values support `{{fieldName}}` variable tokens. Parameters named `objectRefUrn`, `entityApp`, `entityId`, or `entityName` are reserved and are always provided automatically — do not add them here. |

#### Popup

Opens a URL inside a modal popup window within the application, rather than in a new tab. The URL can contain `{{fieldName}}` variable tokens.

| Setting | Description |
| :--- | :--- |
| URL *(required)* | The URL to load inside the popup. Supports asset field variable tokens. |
| Popup Title | Title shown in the popup window header. Supports variable tokens. |
| Size | Small, Medium, Large, or Custom. Choose Custom to set explicit width and height dimensions. Units supported: px, %, em, rem, vw, vh. |
| Enable scrollbars | Whether the popup content area shows scrollbars when content overflows. |

### Options

| Option | Description |
| :--- | :--- |
| Add message to activity stream | When a URL action runs, writes an entry to the asset's activity stream. The message text is set in the **Activity Message** field below it and supports asset field variable tokens. |
| Automatically link to new Asset Types | Partition-scoped and class-scoped actions only. When checked, this action is automatically linked whenever a new asset type is created within the partition. For class-scoped actions, it only links to types whose class matches. This setting also applies when types are moved into the partition from another partition. See [Moving types between partitions](#moving-types-between-partitions). |

## Linking actions to asset types

After an action is created, it must be linked to one or more asset types before it appears on any asset records. Linking is done from the **Linked Asset Types** tab of the action's details form.

* **Linking to specific types**: Select **+ Link to Type**, then select one or more asset types from the list and select **Link Selected**. The action is immediately available on all assets of the selected types.
* **Linking to all types**: Select **Link with All Types** to link the action to all available asset types. If the action is class-scoped, only types of the matching class are linked. If the action is partition-scoped, all types are linked.

## Resetting or disabling

From the Asset Actions panel toolbar, select **Clear All** to delete all actions for this partition and disable the feature. You are asked to type **DELETE** to confirm. Type-specific actions on individual asset types are not affected. After clearing, Custom Buttons resume appearing for assets in this partition.

::: warning
**Clear All is permanent.** Clearing removes all partition-level and class-level actions for this partition. This cannot be undone. Type-specific actions on individual asset types are unaffected.
:::

## Managing actions

Once Asset Actions is enabled for a partition, the Asset Actions panel shows a list of all actions for that partition. From here you can create, edit, delete, and import actions.

![Manage Partition Actions](/_books/servicemanager-config/assets/images/asset-actions-partition-action.png)

### Action options

* **Editing an action**: Select the **Edit** icon or the name of the action on any row in the list. This opens the **Details** and **Linked Asset Types** options. Scope (Partition or Class) is shown as read-only because it can only be set when the action is created.
* **Deleting an action**: Select the **Remove** icon on any action row and confirm in the dialog. Deleting an action removes it from all linked asset types immediately. This cannot be undone.

### Importing from Custom Buttons

If you did not import during the enable step, select **Import** from the toolbar (shown until a Custom Buttons import has been completed for this partition). The import converts your existing Custom Button configuration into Asset Actions:

* Custom buttons with a condition that filters to a single asset type become type-specific actions on that type.
* All other custom buttons become partition-scoped actions and are linked to all existing types.
* Variable tokens are converted from the old `[[fieldName]]` format to `{{fieldName}}` format.
* Group names from Custom Buttons create equivalent action groups per type.

A progress bar tracks the import. Once complete, the Import button is hidden for this partition.

### Importing from another partition

From the toolbar, select **Import > Import from Partition** — shown only when at least one other partition already has actions defined. Select the source partition and select **Import**. All partition-scoped and class-scoped actions from the source are copied into this partition. Copied actions are not linked to any types automatically — link them as needed after the import.

### Using asset field variables

In URL and message fields, select the **Insert variable** button next to the input and select a field from the dropdown. This inserts a token in the format `{{fieldName}}` — for example `{{h_pk_asset_id}}` to pass the asset's unique ID to an external system, or `{{h_name}}` to include the asset name in an activity stream message. At runtime the platform replaces the token with the actual value from the asset record being viewed.

If an action is class-scoped and a field variable you have used is not available for the selected class, a warning panel appears in the form highlighting the affected fields. Review and update these before saving to avoid broken substitutions at runtime.

## Moving types between partitions

Asset types and categories can be moved to a different partition using the **Move Type** or **Move Category** options in Manage Asset Types. When the source partition has Asset Actions enabled, moving a type changes which partition-scoped and class-scoped actions apply to it, so the system automatically updates the action associations as part of the move.

### What happens during a move

When a type (or all types within a category) is moved to a different partition:

1. **Source partition actions are unlinked.** All associations between the type and partition-scoped or class-scoped actions belonging to the *source* partition are removed. Type-specific actions are not affected — they move with the type.
1. **Destination partition actions are auto-linked.** Any partition-scoped or class-scoped actions in the *destination* partition that have **Automatically link to new Asset Types** checked are automatically linked to the moved type. For class-scoped actions, the type's class must match the action's class for the link to be created.

::: warning
**Manual links from the source partition are not preserved.** If a partition-scoped or class-scoped action from the source partition was manually linked to the type (that is, the action does not have auto-associate checked), that link is removed during the move and is not recreated in the destination. After moving, review the type's Actions tab and link any destination partition actions that are needed.
:::

### Warning in the move dialog

If the source partition currently has Asset Actions enabled, a notice is displayed in the Move Type / Move Category dialog before you confirm the move, as a reminder that action associations will change as described above. If Asset Actions has never been enabled for the source partition, no action association changes occur and the notice is not displayed. Either way, the move itself proceeds normally when you select **Move**.

![Move Type](/_books/servicemanager-config/assets/images/asset-actions-move-type.png)

### After moving

After the move completes, navigate to the type's **Actions** tab in its new partition to review the current action list. Actions auto-associated from the destination partition are already present. Use **Add > Link Common Action** to add any additional partition or class actions from the destination partition that were not auto-associated.
