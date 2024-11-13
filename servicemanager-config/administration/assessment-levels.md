# Levels for priority, impact, urgency, and risk
Assessments help users define the importance of a request using the **Assessment** action when viewing a request record.

In Assessments, administrators can configure assessments of type Impact, Urgency, Priority, and Risk. These assessments contain impact levels, urgency levels, priority levels, and risk levels, respectively.

![Assessment types](/_books/servicemanager-config/administration/images/assessment-types.png)

## How to access
Administrators can define assessment levels under the Service Manager configuration.
1. Use the keyboard combination CTRL+SHIFT+S.
1. Search [Configuration](/esp-config/getting-started/using-configuration) for `Assessments`.
1. In the results list, select **Assessments**.

or
1. Select the **Configuration** cog at the bottom of the left-hand application menu bar.
1. In Configuration, from the navigation dropdown, select **Service Manager**.
1. In the navigation panel, scroll to locate the *Administration* section.
1. Click **Assessments**.

## Default levels
Four default levels are provided for each assessment type: Low, Medium, High, and Critical. In the **Levels** tab, you can add new levels, rename and delete levels, and provide translations for the level names.

![Assessment Levels](/_books/servicemanager-config/administration/images/assessment-levels.png)

## Changing the display order
Levels are displayed in picklists for users to select. When you add a new assessment level, it is automatically placed at the bottom of the list. You may want to move the new level to a suitable position. 

**To change the display order of assessment levels:**
1. In Assessments, select an assessment type.
1. In the list of levels, drag and drop the levels into your preferred order using the grab handle icons to the left of each level.

## Priority
Priority is available to any request that is using the Assessment action.  The priority can be viewed as a column in the request list and can be sorted to bring the most important requests to the top of the list.

* The priority can help determine the service level that needs to be applied to a request. 
* The priority can be automatically increased using a service level escalation.
* Within a workflow, the priority can be used to drive communications and the process to take.

## Impact
Impact is currently only available by using an assessment questionnaire. The assessment questionnaire is initiated through a workflow automation.

## Urgency
Urgency is not available on the request's assessment action by default.  There are two options to using the Urgency assessment type:

* Using the following setting, the urgency picklist can be made available on the request's assessment action. This is a global setting and it will apply to all requests.

    |Name|Description|
    |-|-|
    |app.com.hornbill.servicemanager.request.assessment.visibility|This setting enables the urgency selector in the assessment action tab when viewing a request. When this selector is not required, select the `None` option.|

* Urgency can be enabled from a workflow, which includes providing a questionnaire. The benefit of using the workflow automation is that the urgency can be presented at a set point within the workflow.

## Risk
Risk is not available on the request's assessment action by default.  There are two options to using the Risk assessment type:

* Using the following setting, the risk picklist can be made available on the request's assessment action. This is a global setting and it will apply to all requests.

    |Name|Description|
    |-|-|
    |app.com.hornbill.servicemanager.request.assessment.visibility|This setting enables the risk selector in the assessment action tab when viewing a request. When this selector is not required, select the `None` option.|

* Risk can be enabled from a workflow, which includes providing a questionnaire. The benefit of using the workflow automation is that the risk can be presented at a set point within the workflow.

<!-- :::note
If new levels are added when there are existing questions with defined Thresholds, these thresholds will need to be revisited and adjusted to include the new impact level.
:::>