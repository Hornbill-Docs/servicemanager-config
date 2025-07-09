# Custom Lookups
Use the Custom Lookup node in a workflow to assess mapped data that has been setup in a Custom Lookup. A Custom Lookup can be used in place of a decision node when there are larger data sets that need to be compared.

![Custom Lookup Automation](/_books/servicemanager-config/images/workflow-custom-lookup.png)


## Before you begin
* At least one [Custom Lookup](/servicemanager-config/administration/custom-lookups) must be created before this automation can be used.

## Example uses
* Assign a request to a team based on the category that was selected.
* Assign a request to a team based on the location.
* Set the priority, impact, urgency, or risk based on information held in a request.
* Assign an authorizer based on information held in a request.

## Available tasks
* **Get Custom Lookup Information**.  This is the only available task.  This is used to get the information from a selected [Custom Lookup](/servicemanager-config/administration/custom-lookups).

## Options
### Mandatory options
* **Custom Lookup**. Set to `manual` and select one of the available Custom Lookups from the drop-down list.
* **Reference**. Set to `manual` or `variable` and type in the reference to use.  In almost all cases, this will be set to `variable` and the reference will be determined by using the [variable picker](/esp-config/automation/variable-picker) to select a variable from the output of a previous workflow node.