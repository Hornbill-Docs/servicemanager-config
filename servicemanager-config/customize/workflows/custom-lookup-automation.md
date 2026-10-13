# Custom Lookups

Use the Custom Lookup automation in a workflow to assess mapped data that has been set up in a [Custom Lookup](/servicemanager-config/administration/custom-lookups). A Custom Lookup can be used in place of a decision node when there are larger data sets that need to be compared.

![Custom Lookup Automation](/_books/servicemanager-config/images/workflow-custom-lookup.png)

## Before you begin

* At least one [Custom Lookup](/servicemanager-config/administration/custom-lookups) must be created before this automation can be used.

## Example uses

* Assign a request to a team based on the category that was selected.
* Assign a request to a team based on the location.
* Set the priority, impact, urgency, or risk based on information held in a request.
* Assign an authorizer based on information held in a request.

## Available tasks

* **Custom Lookup Details**. This is the only available task. This is used to get the information from a selected [Custom Lookup](/servicemanager-config/administration/custom-lookups).

## Options

### Mandatory options

* **Custom Lookup**. Set to `manual` and select one of the available Custom Lookups from the drop-down list.
* **Reference**. Set to `manual` or `variable` and type in the reference to use. In almost all cases, this will be set to `variable`, and the reference will be determined by using the [variable picker](/esp-config/automation/variable-picker) to select a variable from the output of a previous workflow node.

## Example workflow

![Example Workflow](/_books/servicemanager-config/images/workflow-custom-lookup-example.png)

* **Get Request Information - Category**. This is a standard Get Request Information automation that gets the request category. The category information will be added to an output variable.
* **Custom Lookup - Category->Team**. The Reference option on the Custom Lookup node will use the output variable from the previous node that contains the category information and then use this to look up which team is mapped to that category. The mapped team will be stored in the team output variable.
* **Assign to Team**. The Team option on the Assignment node will use the team output variable from the previous node to make the assignment.

## Output parameters

The following table shows the output parameters that are available from the Custom Lookup automation. The output parameters will only contain a value if the matching entity is included in the [Custom Lookup Reference Record](/servicemanager-config/administration/custom-lookups) being used.

| Custom Lookup Entity | What is returned | Example |
| --- | --- | --- |
| Approver | Approver User ID | grahamc |
| Approver Role | Role Name | Approver Test |
| Approver Team | Team ID | Ares/AISupport/ |
| Closure Category | Category ID | 89 |
| Impact | Impact ID | 9 |
| Priority | Priority ID | 130 |
| Request Category | Category ID | 55 |
| Risk | Risk ID | 3 |
| Service | Service ID | 254 |
| Site | Site ID | 7 |
| Team | Team ID | 1stLineSupport |
| Urgency | Urgency ID | 1 |

In addition to the above output parameters, any custom fields that have been used in a [Custom Lookup](/servicemanager-config/administration/custom-lookups#using-custom-fields-in-custom-lookups) will also be available as output parameters. The name of the output parameter will be the same as the name of the custom field that was used in the Custom Lookup record.
