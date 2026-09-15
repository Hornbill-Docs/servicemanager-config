---
draft: true
---

# Asset Actions

Asset Actions are configurable buttons that appear on asset records. When a user selects one, it can open a URL in a new tab, trigger an Auto Task process, or open a URL inside a popup window — all within the context of the asset being viewed, with the asset's own field values available as variables inside URLs and messages.

## Before you begin

* The **Asset Management Admin** role is required to configure Asset Actions.
* Know how to access the [Service Manager Configuration](/servicemanager-config/index#access-service-manager-configuration).
* Understand how [asset partitions](/servicemanager-config/assets/manage-partitions) and [asset types](/servicemanager-config/assets/manage-asset-types) are structured — actions are scoped to a partition, a class within a partition, or a single asset type.

Asset Actions are enabled and managed **per partition**. When enabled for a partition, Asset Actions replace the legacy Custom Buttons feature for asset records within that partition. Each partition's actions are configured independently.

## Action scope

There are three kinds of action, each with a different scope. All three use the same configuration form — the difference is where you create them and what scope they are assigned. Scope is set when an action is created and cannot be changed afterwards.

* **Partition-scoped actions:** Belong to the partition and can be linked to any asset type within it, regardless of class. Created and managed from the Asset Actions panel inside Manage Asset Types. These are sometimes called *common actions* because they are shared across multiple types. Use this scope for actions that should be available across many or all types in the partition.
* **Class-scoped actions:** Belong to the partition and a specific asset class (for example, Computer or Software). They can only be linked to types of that class within the partition. Use this scope when an action only makes sense for a particular kind of asset.
* **Type-specific actions:** Belong to a single asset type and are created directly from that type's **Actions** tab. They are not shared with any other type, and do not use the scope picker described above.

### How scope affects linking

The scope of an action controls which types appear when you link it:

* **Partition-scoped actions** — the type picker and **Link with All Types** operate across all asset types in the partition.
* **Class-scoped actions** — the type picker and **Link with All Types** show and link only types whose class matches the action's class. Types of other classes are excluded automatically.

Similarly, when viewing a type's **Actions** tab and using **Link Common Action**, only actions relevant to that type are shown: partition-scoped actions for the type's partition, and class-scoped actions whose class matches the type's class. Actions from other partitions or other classes are never shown.

## Enabling Asset Actions

Asset Actions must be enabled separately for each partition. Until enabled, the feature is inactive and Custom Buttons continue to appear for assets in that partition.

![Enable Asset Actions](/_books/servicemanager-config/assets/images/asset-actions-enable.png)

**To enable Asset Actions for a partition:**

1. Navigate to **Configuration > Service Manager > Assets > Manage Types**.
1. Select the partition you want to enable Asset Actions for.
1. In the right-hand panel, select **Asset Actions**. If the feature has not yet been enabled for this partition, the feature overview panel is shown.
1. Choose how you want to start, then select **Enable Asset Actions**:
    * **Enable only** — enables the feature with an empty action list. You build your actions from scratch.
    * **Enable and Import from Custom Buttons** — enables the feature and immediately imports your existing Custom Buttons as Asset Actions. See [Importing from Custom Buttons](#importing-from-custom-buttons) for details of how the import works.
    * **Enable and Import from Partition** — enables the feature and copies all partition-scoped and class-scoped actions from another partition into this one. Select the source partition from the dropdown. Only partitions that already have actions are shown.

Once enabled for a partition, Asset Actions are rendered in place of Custom Buttons on asset records within that partition. Custom Buttons are not deleted — they remain in the Custom Buttons configuration — but they no longer appear while Asset Actions is active.

### Resetting or disabling

From the Asset Actions panel toolbar, select **Clear All** to delete all partition-scoped and class-scoped actions for this partition and disable the feature. You are asked to type **DELETE** to confirm. Type-specific actions on individual asset types are not affected. After clearing, Custom Buttons resume appearing for assets in this partition.

::: warning
**Clear All is permanent.** Clearing removes all partition-level and class-level actions for this partition. This cannot be undone. Type-specific actions on individual asset types are unaffected.
:::

## Managing partition actions

Once Asset Actions is enabled for a partition, the Asset Actions panel shows a list of all partition-scoped and class-scoped actions for that partition. From here you can create, edit, delete, and import actions.

![Manage Partition Actions](/_books/servicemanager-config/assets/images/asset-actions-partition-action.png)

### Creating an action

1. In the Asset Actions panel, select **Add Action**.
1. The inline edit form opens. Set the scope (see [Action scope](#action-scope)), then fill in the display fields, action type settings, and options.
1. Select **Save**. The action is created and appears in the list.
1. The action now exists but is not linked to any asset types. Go to the relevant asset type's **Actions** tab and use **Add > Link Common Action** to link it, or select **Edit** on the action and use the **Linked Types** tab to link it to one or more types.

After saving, an action does not appear on any asset records until it is linked to one or more types — the exception is actions with **Automatically associate to new Asset Types** checked, which are linked automatically when a new type is created.

### Editing a partition or class action

Select **Edit** on any action row in the list. The full-page edit form opens in a new tab, showing a **Details** tab and a **Linked Types** tab. Changes to the configuration (label, URL, icon, and so on) are shared across all types that use the action. Scope (Partition or Class) is shown as read-only here — it's set when the action is first created and cannot be changed; delete the action and create a new one if you need a different scope.

### Deleting an action

Select **Remove** on any action row and confirm in the dialog. Deleting an action removes it from all linked asset types immediately. This cannot be undone.

### Importing from Custom Buttons

If you did not import during the enable step, select **Import** from the toolbar (shown until a Custom Buttons import has been completed for this partition). The import converts your existing Custom Button configuration into Asset Actions:

* Custom buttons with a condition that filters to a single asset type become type-specific actions on that type.
* All other custom buttons become partition-scoped actions and are linked to all existing types.
* Variable tokens are converted from the old `[[fieldName]]` format to `{{fieldName}}` format.
* Group names from Custom Buttons create equivalent action groups per type.

A progress bar tracks the import. Once complete, the Import button is hidden for this partition.

### Importing from another partition

From the toolbar, select **Import > Import from Partition** — shown only when at least one other partition already has actions defined. Select the source partition and select **Import**. All partition-scoped and class-scoped actions from the source are copied into this partition. Copied actions are not linked to any types automatically — link them as needed after the import.

## Configuring an action

The action form — both the inline partition panel editor and the full-page editor opened from the edit button — contains three configuration sections: Display, Action, and Options.

![Configure Actions](/_books/servicemanager-config/assets/images/asset-actions-configure-action.png)

### Display

| Field | Description |
| :--- | :--- |
| Scope | Shown when creating a new action. Select **Partition** or **Class**; for Class, also select the asset class from the dropdown that appears. Read-only when editing an existing action. |
| Label *(required unless an icon is set)* | The text shown on the button. |
| Description | Text shown when a user hovers over the button. Optional but recommended for less obvious actions. |
| Button Style | The color style for the button: Default (gray), Primary (blue), Success (green), Danger (red), Warning (yellow), Info (light blue). |
| Icon | A FontAwesome icon displayed alongside the button label, chosen using the icon picker. Optional. |

### Action

Select the action type and complete the fields that appear for it. See [Action types](#action-types) for details on each type.

### Options

| Option | Description |
| :--- | :--- |
| Add message to activity stream | When a URL action runs, writes an entry to the asset's activity stream. The message text is set in the **Activity Message** field below it and supports asset field variable tokens. |
| Automatically associate to new Asset Types | Partition-scoped and class-scoped actions only. When checked, this action is automatically linked whenever a new asset type is created within the partition. For class-scoped actions, it only links to types whose class matches. This setting also applies when types are moved into the partition from another partition — see [Moving types between partitions](#moving-types-between-partitions). |

### Using asset field variables

In URL and message fields, select the **Insert variable** button next to the input and select a field from the dropdown. This inserts a token in the format `{{fieldName}}` — for example `{{h_pk_asset_id}}` to pass the asset's unique ID to an external system, or `{{h_name}}` to include the asset name in an activity stream message. At runtime the platform replaces the token with the actual value from the asset record being viewed.

If an action is class-scoped and a field variable you have used is not available for the selected class, a warning panel appears in the form highlighting the affected fields. Review and update these before saving to avoid broken substitutions at runtime.

## Action types

### URL

Opens a URL in a new browser tab. The URL can contain `{{fieldName}}` variable tokens. Use this to link to an external system, a deep link elsewhere in the platform, or any web address relevant to the asset.

If the URL does not include a protocol (`://`), `http://` is automatically prepended at runtime.

**Required:** URL field.

The optional **Activity Message** field (under Options) allows a note to be written to the asset's activity stream each time this action is triggered. The message supports variable tokens and is written after the URL is opened.

### Auto Task

Triggers an Auto Task when the user selects the button. The asset's URN is automatically passed as the `objectRefUrn` input parameter so the Auto Task knows which asset it is operating on.

| Setting | Description |
| :--- | :--- |
| Auto Task Name *(required)* | The exact name of the Auto Task process to trigger. Select from the dropdown list of available processes. |
| Open popup with Auto Task progress | Shows a modal window that tracks the Auto Task as it runs, matching the progress view shown by the existing Custom Buttons feature. |
| Display Auto Task progress in timeline | Posts a link to the started Auto Task in the asset's activity stream, giving a record of when the action was triggered. |
| Prompt for confirmation before running | Shows a confirmation prompt before the Auto Task starts. You can customize the prompt text (for example, *"Are you sure you want to retire this asset?"*). |
| Additional input parameters | A table of extra key/value pairs passed as BPM input parameters alongside the standard asset fields. Values support `{{fieldName}}` variable tokens. Parameters named `objectRefUrn`, `entityApp`, `entityId`, or `entityName` are reserved and are always provided automatically — do not add them here. |

### Popup

Opens a URL inside a modal popup window within the application, rather than in a new tab. The URL can contain `{{fieldName}}` variable tokens.

| Setting | Description |
| :--- | :--- |
| URL *(required)* | The URL to load inside the popup. Supports asset field variable tokens. |
| Popup Title | Title shown in the popup window header. Supports variable tokens. |
| Size | Small, Medium, Large, or Custom. Choose Custom to set explicit width and height dimensions. Units supported: px, %, em, rem, vw, vh. |
| Enable scrollbars | Whether the popup content area shows scrollbars when content overflows. |

## Actions on an asset type

Navigate to **Manage Types**, select a type, and select the **Actions** tab. This tab has two panels:

![Action Tab](/_books/servicemanager-config/assets/images/asset-actions-action-tab.png)

* **Preview panel** (top) — search for an asset of this type using the autocomplete picker and see a live preview of how the action buttons render on that asset's record. Toggle between **Full** and **Compact** width to preview both the expanded button layout and the collapsed "Actions" dropdown.
* **Action list** (below) — the full list of actions and groups for this type, in their current display order. Drag rows to reorder.

### Adding an action

Select **Add**. A dropdown appears with three options:

* **Create Type Action** — opens the action configuration popup. Fill in the form and save to create a new action that belongs exclusively to this asset type.
* **Link Common Action** — opens a picker showing common actions that can be linked to this type. The list is filtered automatically to only show partition-scoped actions belonging to this type's partition, and class-scoped actions whose class matches this type's class. Actions from other partitions or that belong to a different class are never shown. Select one or more and select **Link Selected**. A progress bar tracks the operation when linking multiple actions.
* **Add Group** — prompts for a group name and creates a new action group. See [Action groups and order](#action-groups-and-order).

### Editing an action on a type

Select **Edit** on any action row:

* **Type-specific actions** — the configuration popup opens inline. Changes affect only this type.
* **Partition-scoped and class-scoped actions** — selecting **Edit** opens the full-page edit form in a new browser tab. You are editing the shared configuration that every linked type uses. Ordering, grouping, and position on this specific type are controlled separately, from the action list on the type's Actions tab.

### Linking visibility

A partition-scoped or class-scoped action only appears on an asset type if it has been explicitly linked to that type. Linking creates a position record; without one, the action is not visible on those assets.

The **Automatically associate to new Asset Types** toggle (on the action form, under Options) controls what happens when a new asset type is created:

* **Checked** — a position record is automatically created for this action on the new type. The action is visible immediately. For class-scoped actions, auto-association only applies when the new type's class matches the action's class.
* **Unchecked** — no automatic link. The action does not appear on the new type until explicitly linked from the type's Actions tab.

The **Linked Types** tab on the full-page action editor shows all types currently linked to the action. Three toolbar operations are available:

* **Link to Type** — opens a type picker to link the action to one or more types. For partition-scoped actions, all types in the partition are shown (filterable by category). For class-scoped actions, only types whose class matches the action's class are shown.
* **Link with All Types** — links the action to every eligible type not already linked. For partition-scoped actions, this covers all types in the partition. For class-scoped actions, only types of the matching class are linked.
* **Remove from All Types** — removes all links. The action no longer appears on any type.

### Removing an action from a type

Select the **Unlink** / **Delete** button on an action row and confirm in the dialog. The behavior differs by action scope:

* **Type-specific actions** — permanently deleted.
* **Partition-scoped and class-scoped actions** — unlinked from this type only. The action continues to exist and remains visible on other types it is linked to.

## Action groups and order

### Action groups

Groups let you organize multiple actions into a single dropdown button on the asset record. Instead of showing several individual buttons, the asset displays one button with the group's name; selecting it opens a menu listing all actions in that group.

![Action Groups](/_books/servicemanager-config/assets/images/asset-actions-action-group.png)

Groups are per-type: the same action can be in different groups (or no group) on different asset types. Grouping is configured from each type's **Actions** tab and does not affect other types.

**To create a group:**

1. On the type's **Actions** tab, select **Add** and choose **Add Group**.
1. Enter the group name. This becomes the label on the dropdown button on the asset record.
1. Drag existing action rows into the group, or use **Add** within the group to create or link actions directly inside it.

**To rename a group:** Select **Rename** on the group header, enter a new name in the inline input, and press Enter or select away. The change saves immediately.

**To delete a group:** Select **Delete** on the group header and confirm. Actions inside the group are not deleted — they move out of the group and appear ungrouped in the list.

### Action order

The order of actions on the asset record is set per type from the **Actions** tab. Each action row and each group header has a drag handle on the left. Drag a row to a new position; the updated order saves automatically when you release it.

You can drag actions between groups (including out of a group entirely), and drag groups relative to one another and to ungrouped actions. Each type has its own completely independent action order — the same action can be first on one type and last on another, so configure ordering separately on each type's Actions tab.

When you create or link an action, it is placed at the end of the list for that type. Drag it to the correct position once it appears.

## Moving types between partitions

Asset types and categories can be moved to a different partition using the **Move Type** or **Move Category** options in Manage Asset Types. When the source partition has Asset Actions enabled, moving a type changes which partition-scoped and class-scoped actions apply to it, so the system automatically updates the action associations as part of the move.

### What happens during a move

When a type (or all types within a category) is moved to a different partition:

1. **Source partition actions are unlinked.** All associations between the type and partition-scoped or class-scoped actions belonging to the *source* partition are removed. Type-specific actions are not affected — they move with the type.
1. **Destination partition actions are auto-associated.** Any partition-scoped or class-scoped actions in the *destination* partition that have **Automatically associate to new Asset Types** checked are automatically linked to the moved type. For class-scoped actions, the type's class must match the action's class for the link to be created.

::: warning
**Manual links from the source partition are not preserved.** If a partition-scoped or class-scoped action from the source partition was manually linked to the type (that is, the action does not have auto-associate checked), that link is removed during the move and is not recreated in the destination. After moving, review the type's Actions tab and link any destination partition actions that are needed.
:::

### Warning in the move dialog

If the source partition currently has Asset Actions enabled, a notice is displayed in the Move Type / Move Category dialog before you confirm the move, as a reminder that action associations will change as described above. If Asset Actions has never been enabled for the source partition, no action association changes occur and the notice is not displayed. Either way, the move itself proceeds normally when you select **Move**.

![Move Type](/_books/servicemanager-config/assets/images/asset-actions-move-type.png)

### After moving

After the move completes, navigate to the type's **Actions** tab in its new partition to review the current action list. Actions auto-associated from the destination partition are already present. Use **Add > Link Common Action** to add any additional partition or class actions from the destination partition that were not auto-associated.
