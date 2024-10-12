# Assessment Levels
Assessment Levels help define the importance of a request.  These levels can be allocated to three types of assessment which include priority, impact, and urgency.  Levels can be applied to a request using the `Assessment` action when viewing a request record.

## How To Access
Assessment Levels are defined under the Service Manager configuration.
1. On the keyboard use the key combination `Ctrl+Shift+s`.
1. Search [Configuration](/esp-config/getting-started/using-configuration) for *Assessment*.
1. In the results list select `Assessments`.

or

1. Open configuration and select `Service Manager` from the navigation dropdown.
2. In the navigation panel locate the section titled *Administration*.
3. Select `Assessments`.
4. Select the `Levels` tab.

## Default Levels
Four default levels are provided for each assessment type. This includes Low, Medium, High, and Critical. The `Levels` tab provides options to delete, add, rename, and provide translations for the available levels.

![Assessment Levels](_books/servicemanager-config/administration/images/assessment-levels.png)

## Changing the Order
On the left side of each level, an icon is visible that allows you to drag and drop to change the order in they are displayed in picklists, where they are selected.  This is commonly used when adding new levels.  A new level will be automatically placed at the bottom of the list.  You can then move the new level to a suitable position.

## Priority
Priority is available to any request that is using the Assessment action.  The priority can be viewed as a column in the request list and can be sorted to bring the most important requests to the top of the list.

* The priority can help determine the service level that needs to be applied to a request. 
* The priority can be automatically increased using a service level escalation.
* Within a workflow, the priority can be used to drive communications and the process to take.

## Impact
Impact is currently only available by using an assessment questionnaire. The assessment questionnaire is initiated through a workflow automation.

## Urgency
Urgency is not available on the request's assessment action by default.  There are two options to using urgency.

Using the following setting, the urgency picklist can be made available on the request's assessment action. This is a global setting and it will apply to all requests.

|Name|Description|
|-|-|
|app.com.hornbill.servicemanager.request.assessment.visibility|This setting enables the urgency selector in the assessment action tab when viewing a request. When this selector is not required, select the 'None' option.|

Urgency can be enabled from a workflow, which includes providing a questionnaire. The benefit of using the workflow automation is that the urgency can be presented at a set point within the workflow.

<!-- :::note
If new levels are added when there are existing questions with defined Thresholds, these thresholds will need to be revisited and adjusted to include the new impact level.
:::>