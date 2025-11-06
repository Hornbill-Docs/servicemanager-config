# Asset Automation
This automation is specific to an asset entity, which can be used as part of an [Auto Task](/servicemanager-config/customize/service-manager-auto-tasks) on an asset or from a request workflow.

## Get Asset Information
Use this node to get information about a specified asset.  Once the information about an asset is available to the auto task or workflow, this information can be used with decision nodes 

![Asset Automation](/_books/servicemanager-config/images/workflow-asset-get-info.png)

#### Available Tasks
Selecting a task will determine the available output variables.  The Basic Asset Task can be used to get the basic details that are available on all assets.  All the other available tasks refer to specific asset classes.
* Basic Asset
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

#### Options
##### Mandatory Options
* **Asset ID**. The assit ID is a required field. When this automation is being used on an auto task that is connected to an asset record using a custom button, this can be set to Auto.  When this automation is used on a request workflow, this must be set to either Manual or Variable, and the asset ID must be provided using one of these mechanisms.