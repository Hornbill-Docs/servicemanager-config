# Manage asset substates
Asset states tell you where an asset is in its lifecycle (e.g., *Current*, *Active*, *Archived*). With substates, you can add a customizable layer of detail within those states, allowing you to reflect more specific conditions or workflows.

For example:
* State: Current → Substate: In Stock (for assets awaiting allocation).
* State: Active → Substate: Allocated (for assets assigned to users).

The purpose of substates is to enhance tracking, searching, and reporting by providing more granularity, making it easier to manage assets based on their exact condition or stage.

Substates are global, so you can define them for each state across all asset types.

While asset states are fixed, asset substates are not fixed; you can create new substates under asset states as needed. You control the visibility of both asset states and asset substates for each asset type. You also control whether the state and substate fields are mandatory and read-only.

**To add an asset substate:**
1. Navigate to **Configuration > Service Manager > Assets > Manage Substates**.
1. In the list of states (Current, Active, Archived), in the row of the state for which you want to create a substate, click **Create** (the plus sign).
1. In the Create Substate dialog, give your new substate a name and click **Create**.

**To make an asset state or substate visible or hidden:**
1. Navigate to **Configuration > Service Manager > Assets > Manage Types**.
1. In Asset Categories, select an asset type for which you have added asset states or substates.
1. Click the List Fields tab.
1. In the Available Asset List Columns, for the state or substate you want to control visibility, toggle the eye icon ON or OFF.

**To make an asset state or substate mandatory and/or read-only:**
1. Navigate to **Configuration > Service Manager > Assets > Manage Types**.
1. In Asset Categories, select an asset type for which you have added asset states or substates.
1. Click the Detail Fields tab.
1. In the list of fields, in the row of the state or substate field, click **Field Properties** (the cog icon).
1. In the State dialog, in the *Read-only* dropdown, select Yes or No.
1. In the State dialog, in the *Mandatory* dropdown, select Yes or No.
1. Click **Save Changes**.