# Asset Automation
This automation is specific to an asset entity, which can be used as part of an [Auto Task](/servicemanager-config/customize/service-manager-auto-tasks) on an asset or from a request workflow.

## Get Asset Information
Retrieve data for a specific asset to use in decision nodes or subsequent workflow steps.

![Asset Automation](/_books/servicemanager-config/images/workflow-asset-get-info.png)

### Available tasks

The selected task determines the available output variables. Use **Basic Asset** or **Get Asset Custom Properties** for attributes common to all assets. Other tasks retrieve data specific to asset classes:

* Basic Asset
* Get Asset Custom Properties
* Get Computer Peripheral Asset Details
* Get Computer System Asset Details
* Data Processing Record Asset
* Mobile Device Asset
* Network Circuit Asset
* Network Device Asset
* Printer Asset
* Software Asset
* System Asset
* Telecoms Asset

### Options

#### Mandatory options

*   **Asset ID**: The unique identifier for the asset. 
    *   For an **Auto Task** triggered by a custom button on an asset record, set this to **Auto**. 
    *   For a request workflow, set this to **Manual** or **Variable** and provide the ID through that mechanism.