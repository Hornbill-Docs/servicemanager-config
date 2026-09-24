# Services Automation

The Services Automation lets you define tasks that are related to the Service entity.  

![Services automation](/_books/servicemanager-config/images/workflow-services-status.png)

## Before you begin

* Read about [service dependencies](/servicemanager-user-guide/service-portfolio/services/service-dependancies).
* Read about the [request service automation](/servicemanager-config/customize/workflows/requests-automation#request-service).
* Read about [service bulletins](/servicemanager-user-guide/service-portfolio/services/service-bulletins).

---
## Bulletin

Service bulletins can be displayed on the Employee and Customer portals under the service pages that they relate to. The Employee Portal can also use the [Bulletins widget](/esp-config/customize/employee-portal/employee-portal-widgets#bulletins-widget) to display these.

### Create

This task is responsible for creating a new bulletin for a service.

#### Create bulletin options

* **Service** - This is a mandatory input for this workflow operation. It is required to determine under which service the bulletin will be created. If this input is not provided, the operation will fail. When configuring this input, the manual option provides a list of services. When a service is selected, the ID of that service is passed as the input value. If the Service input is configured using free text or a variable, make sure the value provided is the ID of an existing service, not the service name.
* **Title** - The title of the newly created bulletin. The title field has a maximum length of 255 characters. If a title longer than 255 characters is provided, the workflow will truncate the value and use only the first 255 characters.
* **Description** - The description of the new bulletin.
* **Display Bulletin Text** - (Yes|No). Option to display the title and description text on the bulletin.
* **Display Bulletin Text Shadow** - (Yes|No). Display the bulletin text title with a shadow. This only applies if the "Display Bulletin Text" option is set to `Yes`.
* **Visibility Start** - The start time of the bulletin. Make sure to provide a valid date format for this input. Providing an incorrect date value will cause the workflow operation to fail, and the bulletin will not be created.
* **Visibility End** - The end time of the bulletin. Make sure to provide a valid date format for this input. Providing an incorrect date value will cause the workflow operation to fail, and the bulletin will not be created.
* **Employee Portal Link** - A link used when viewing the bulletin in the employee portal. This field has a maximum length of 255 characters. If a link longer than 255 characters is provided, the workflow operation will not set any link for the bulletin.
* **Status** - The bulletin status (draft|publish|retire). The default value is draft. If no status is provided, or if the provided status is different from publish/published or retire/retired, the status is automatically set to draft.
* **Language** - The bulletin language. Defaults to en-GB. To use a different language, specify a language code supported by your instance, for example, de or fr.
The manual option shows a list of all supported languages in the instance. When a language is selected, its language code is passed as the input value.
If the input is configured using a variable, make sure to pass a supported language code. Passing an invalid language code will cause the workflow operation to fail, and the bulletin will not be created. Passing a valid but unsupported language code will make the bulletin inaccessible until that language is supported in the instance.
* **Create Default English Version** - Creates a default English version of the bulletin. This option applies only if the bulletin is created in a language other than English.

##### Outputs

* **Bulletin ID** - The ID of the created bulletin.
* **Outcome** - The operation outcome (success | failure).

### Delete

This workflow operation is responsible for deleting a bulletin.

#### Delete bulletin options

* **Bulletin** - This is a mandatory input for this workflow operation. It is required to determine which bulletin will be deleted. When configuring this input, the manual option provides a list of default bulletins. When a bulletin is selected, its ID is passed as the input value. If the Bulletin input is configured using free text or a variable, make sure the value provided is a valid bulletin ID. If the provided bulletin ID belongs to the default bulletin (to which all translations are linked), this workflow operation deletes the default bulletin and all its translations.
If the provided bulletin ID belongs to a translated version, only that specific translation is deleted.

##### Outputs

* **Outcome** - The operation outcome (success | failure).

---

### Update

This workflow operation is responsible for updating an existing bulletin.

#### Options

* **Bulletin** - This is a mandatory input for this workflow operation. It is required to determine which bulletin will be updated. When configuring this input, the manual option provides a list of default bulletins. When a bulletin is selected, its ID is passed as the input value. If the Bulletin input is configured using free text or a variable, make sure the value provided is a valid bulletin ID.
* **Title** - The new title for the bulletin. The title field has a maximum length of 255 characters. If a title longer than 255 characters is provided, the workflow will truncate the value and use only the first 255 characters. If this input is set to Auto or Ignore, the bulletin title will not be changed.
* **Description** - The new description for the bulletin. If this input is set to Auto or Ignore, the description will not be changed.
* **Display Bulletin Text** - (Yes|No). Option to display the title and description text. If this input is set to Auto or Ignore, the value will not be changed.
* **Display Bulletin Text Shadow** - (Yes|No). Option to display the bulletin text title shadow. If this input is set to Auto or Ignore, the value will not be changed.
* **Visibility Start** - The start time of the bulletin. Make sure to provide a valid date format. Providing an incorrect date value will cause the workflow operation to fail. If this input is set to Auto or Ignore, the Visibility Start value will not be changed.
* **Visibility End** - The end time of the bulletin. Make sure to provide a valid date format. Providing an incorrect date value will cause the workflow operation to fail.
If this input is set to Auto or Ignore, the Visibility End value will not be changed.
* **Employee Portal Link** - A link used when viewing the bulletin in the employee portal. This field has a maximum length of 255 characters. If this input is set to Auto or Ignore, or if the provided value exceeds 255 characters, the link will not be updated.
* **Status** - (draft|publish|retire). Change the status of the bulletin. If no status is provided, or if the provided status is not one of publish/published, retire/retired, or draft, the status will not be updated.
* **Language** - The bulletin language. Defaults to en-GB. To use a different language, specify a language code supported by your instance, for example, de or fr.
The manual option shows a list of all supported languages in the instance. When a language is selected, its language code is passed as the input value.
If the input is configured using a variable, make sure to pass a supported language code. Passing an invalid language code will cause the workflow operation to fail, and the bulletin will not be updated.
Passing a valid but unsupported language code will make the bulletin inaccessible until that language is supported in the instance.

#### Outputs

* **Outcome**. The operation outcome (success|failure).

---

## Update related services

### Status

The service status can help both the support staff and users on the portals to identify when a service is impacted or unavailable. The changes in service status can also contribute to the service [availability metrics](/servicemanager-user-guide/service-portfolio/services/service-availability#availability-metrics).

#### Options

* **Request ID** - This is a mandatory option, but in most cases it should be set to `Auto`, which automatically picks up the request ID from the request that the workflow is running on.
* **Relationship Type** - This option sets the status update based on the dependency between the request's service and that service's dependencies. The default is set to `Ignore`, which will apply the status change to all services, independent of the dependency. The dependency options include:
  * Related and Request Service depend on each other
  * Request Service depends on Related
  * Related depends on Request Service
* **Related Services Type** - Select if the status update will apply to Business, Technical, or both Business and Technical services.
* **Status**. This is a mandatory option.  This needs to be set to `Manual`, and then one of the available statuses needs to be selected.

:::tip
The related services do not need to be added as a related service on the request for the status to be updated.
:::

---

## Update the status of services by service ID

This workflow operation updates the status and status message of one or more services, identified by their service ID.

The service does not need to be the service of a request, or be linked to a request in any way. This makes the operation suitable for major incident and service status workflows, where the services affected are chosen during the process, for example by an analyst during Intelligent Capture or through a task.

The status set by this operation is the same service status that can be changed manually from the service in the Service Portfolio. It is shown to analysts and to service subscribers on the portals, and changes in status contribute to the service [availability metrics](/servicemanager-user-guide/service-portfolio/services/service-availability#availability-metrics).

#### Options

* **Service(s)** - This is a mandatory input. It determines which services are updated.
  * When set to **Manual**, a list of the services you can access in the Service Portfolio is provided. For administrators this includes services that are in the pipeline or retired. Each service is shown with its name followed by its ID, for example `HR Service (ID:1001)`, so services with the same name can be told apart. One service can be selected.
  * To update more than one service, or to use a value captured earlier in the workflow, set this input to **Variable**. The value can be a single service ID, a list of service IDs separated by commas, for example `1001,1002,1003`, or the answer of a checkbox field that holds service IDs.
  * Always use the service ID shown in the Service Portfolio. Service names are not accepted.
* **Status** - This is a mandatory input. The status to apply to every service supplied. The available statuses are taken from the service status list, including any custom statuses that have been added to it.
* **Status Message** - An optional message describing the status, which is shown alongside the status. If no message is provided, the default message for the selected status is used, for example "This Service is currently Unavailable". Custom statuses do not have a default message, so a message is recommended when using one.

#### Outputs

* **Outcome** - The outcome of the operation (success | failure). The outcome is `failure` when no service could be updated, or when the status provided is missing or not recognized.
* **Services Updated Count** - The number of services that now have the requested status and message. This includes services that already had them.
* **Error Message** - A list of the service IDs that could not be updated, with the reason, for example when a service ID does not exist.

#### How the operation behaves

* **Services already in the requested state** are left as they are. They are still counted in the Services Updated Count, and no change is recorded against them.
* **Changing only the message** of a service that already has the requested status updates the message. As the status itself has not changed, no new entry is added to the service availability data.
* **Leaving the Status Message empty** always applies the default message for the status. If a service currently shows a custom message and the same status is applied again without a message, the custom message is replaced by the default message.
* **Service IDs that cannot be found** are skipped and listed in the Error Message output. The remaining services are still updated.
* **Duplicate service IDs** in the same list are only updated once.
* **When nothing is supplied** in the Service(s) input, no service is updated and the outcome is `success`.
* **Services in other languages.** The status belongs to the service rather than to a translation, so the same status and message are shown to users in every language.

:::tip
The same status is applied to every service supplied to one operation. To set different statuses on different services, for example one service Impacted and another Unavailable, add one operation for each status.
:::

:::tip
Use the Outcome and Error Message outputs in a decision node to notify someone, or to take another path in the workflow, when a service could not be updated.
:::

:::note
A page that is already open, such as a service in the Service Portfolio, shows the new status after it is refreshed.
:::

#### Example: major incident workflow

1. When a major incident is raised, the analyst selects the impacted service in Intelligent Capture.
2. A **Status > Update** operation uses the captured service to set its status to **Unavailable**, with a message such as "Engineers are investigating. Next update in 30 minutes."
3. A recurring human task lets the analyst add further affected services as the incident develops, each one updated by another **Status > Update** operation.
4. When the incident is resolved, a final **Status > Update** operation sets the same services back to **Available**, which restores the default message.

Throughout the incident, the status and message are shown on the portals to users of the affected services, and the time spent in each status is recorded in the service availability metrics.
