# Asset automation

Asset automation allows you to perform actions on asset entities. You can use these automations as part of an [Auto Task](/servicemanager-config/customize/service-manager-auto-tasks) on an asset record or within a request workflow.

## Get asset information

Use this task to retrieve data from a specific asset record. You can use the information you retrieve in decision nodes or other workflow steps later in your process.

![Get Asset Information automation](/_books/servicemanager-config/images/workflow-asset-get-info.png)

### Before you begin

Ensure you have the **Asset ID** for the record you want to access.

### Steps

1. Select the task that matches the type of data you need. The task you choose determines which output variables are available.
   * **Basic Asset**: Use this for attributes common to all assets.
   * **Get Asset Custom Properties**: Use this for custom attributes.
   * **Get Computer Peripheral Asset Details**
   * **Get Computer System Asset Details**
   * **Data Processing Record Asset**
   * **Mobile Device Asset**
   * **Network Circuit Asset**
   * **Network Device Asset**
   * **Printer Asset**
   * **Software Asset**
   * **System Asset**
   * **Telecoms Asset**
2. In the **Asset ID** field, specify the unique identifier for the asset.
   * If you are creating an **Auto Task** triggered by a custom button on an asset record, set this to **Auto**.
   * If you are creating a request workflow, set this to **Manual** or **Variable** and provide the ID.

## Manage shared users

Use these tasks to control which users are associated with a specific asset.

![Shared Users automation](/_books/servicemanager-config/images/workflow-asset-shared-users.png)

### Available tasks

* **Get Shared Users**: Retrieve the list of users currently shared with an asset.
* **Add Shared User**: Connect a new user to an asset.
* **Remove Shared User**: Disconnect an existing user from an asset.

### Steps

1. Select the shared user task you want to perform.
2. In the **Asset ID** field, enter or select the unique identifier for the asset.
3. If you selected **Add Shared User** or **Remove Shared User**, enter the unique identifier for the user in the **User ID** field.

<!-- #JA[Visual Cue: Annotated screenshot of the Asset Automation configuration screen highlighting the Asset ID and User ID input fields.] -->
