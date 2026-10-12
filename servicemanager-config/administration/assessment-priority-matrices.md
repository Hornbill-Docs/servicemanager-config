# Priority Matrices

A priority matrix is a standardized grid used by service desks to eliminate guesswork by calculating a request's priority based on two strict variables: Impact (the scope of business disruption) and Urgency (the time sensitivity of the issue). By cross-referencing these, the matrix automatically assigns a priority. This approach removes human bias and ensures that requests are responded to appropriately.

## Before you begin

* To manage the priority matrix, you must have the [Service Desk Admin](/servicemanager-config/setup/service-manager-roles#administration-roles) role.
* The [Assessment Levels](/servicemanager-config/administration/assessment-levels) must be configured with appropriate priority, impact and urgency levels.
* [Questionnaires](/servicemanager-config/administration/assessment-questionnaires) must be configured before they can be applied to a priority matrix.

## Access priority matrices configuration

Administrators can access the priority matrices through the Service Manager configuration.

### Use global search

1. Press **CTRL+SHIFT+S**.
2. Search for `Assessments`.
3. Select **Assessments** from the results list.
4. Select the **Priority Matrices** tab.

### Use the navigation menu

1. Select the **Configuration** cog icon at the bottom of the left navigation menu.
2. Select **Service Manager** from the navigation dropdown.
3. Scroll to the **Administration** section.
4. Select **Assessments**.
5. Select the **Priority Matrices** tab.

## Creating a priority matrix

### Details

* **Name**: The name of the priority matrix. This name is used to identify the matrix in the list of priority matrices. This list is used on the details of a Service and on items in the Request Catalog for that Service. It is important to provide a name that is descriptive of its purpose.
* **Status**: The status of the priority matrix. The status can be set to **Active** or **Inactive**. Only active matrices are available for use in the system.
* **Use Impact Questionnaire**: If selected, a user will be presented with the questionnaire rather than selecting an impact level from a list.
* **Use Urgency Questionnaire**: If selected, a user will be presented with the questionnaire rather than selecting an urgency level from a list.
* **Use Priority Questionnaire**: If selected, when the priority override is enabled, the user will be presented with the questionnaire rather than selecting a priority level from a list.
* **Allow Manual Priority Override**: If selected, the priority matrix will allow the priority level of a request to be manually overridden. If not selected, the priority level of a request will be determined by the priority matrix.

### Matrix

The matrix is a grid that defines the priority level for each combination of impact and urgency levels. The matrix is configured by selecting the appropriate priority level for each combination of impact and urgency levels.

![Priority Matrix](/_books/servicemanager-config/administration/images/priority-matrix.png)

Each cell in the matrix represents a combination of impact and urgency levels. The priority level for each combination is set by clicking on the cell and selecting the appropriate priority level.

> **Note**: If an impact or urgency questionnaire is used, make sure that the impact and urgency levels configured in the questionnaire match the levels used in the priority matrix.
