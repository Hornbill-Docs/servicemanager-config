# Assessment levels

Assessments allow users to define request importance using the **[Assessment](/servicemanager-user-guide/service-portfolio/requests/assessment-action)** action. Administrators configure assessments for **Impact**, **Urgency**, **Priority**, and **Risk**. Each type contains configurable levels to categorize requests.

![Assessment types](/_books/servicemanager-config/administration/images/assessment-types.png)

## Access assessment configuration

Administrators can access assessment level settings through the Service Manager configuration.

### Use global search

1. Press **CTRL+SHIFT+S**.
2. Search for `Assessments`.
3. Select **Assessments** from the results list.

### Use the navigation menu

1. Select the **Configuration** cog icon at the bottom of the left navigation menu.
2. Select **Service Manager** from the navigation dropdown.
3. Scroll to the **Administration** section.
4. Select **Assessments**.

## Manage assessment levels

Each assessment type includes four default levels: Low, Medium, High, and Critical. Use the **Levels** tab to add, rename, or delete levels. You can also provide translations for level names in this tab.

![Assessment Levels](/_books/servicemanager-config/administration/images/assessment-levels.png)

### Change the display order

Levels appear in fields in the order defined in the configuration. New levels are added to the bottom of the list by default.

1. In **Assessments**, select an assessment type.
2. In the levels list, use the grab handle icons to the left of each level to drag and drop them into the preferred order.

## Assessment types

### Priority

Priority is available for any request using the **Assessment** action.

* **Visibility:** Priority appears as a column in the request list and supports sorting.
* **Service Levels:** Priority helps determine the service level applied to a request.
* **Escalation:** Service level escalations can automatically increase priority.
* **Workflows:** Priority drives communication logic and process branching within a workflow.

### Impact

Impact is available only through assessment questionnaires. Workflow automation initiates these questionnaires.

### Urgency

Urgency is disabled on the request **Assessment** action by default. Use one of the following methods to enable it:

* **Global Setting:** Enable the urgency selector for all requests by configuring the following setting:

| Name | Description |
| :--- | :--- |
| `app.com.hornbill.servicemanager.request.assessment.visibility` | Enables the urgency selector in the assessment action tab. Set to `None` to hide the selector. |

* **Workflow Automation:** Enable urgency via a workflow questionnaire. This method allows the urgency assessment to appear at a specific stage in the process.

### Risk

Risk is available only through assessment questionnaires. Workflow automation initiates these questionnaires.

:::important
If you add new levels to an assessment type that has existing questions with defined thresholds, you must update those thresholds to include the new levels.
:::
