# Services Automation

The Services Automation lets you define tasks that are related to the Service entity.  

![Services automation](/_books/servicemanager-config/images/workflow-services-status.png)

## Before you begin
* Read about [service dependancies](/servicemanager-user-guide/service-portfolio/services/service-dependancies).
* Read about the [request service automation](/servicemanager-config/customize/workflows/requests-automation#request-service).
* Read about [service bulletins](/servicemanager-user-guide/service-portfolio/services/service-bulletins).

## Bulletin
Service bulletins can be displayed on the Employee Portal, using the [Bulletins widget](/esp-config/customize/employee-portal/employee-portal-widgets#bulletins-widget), and they are available on each service page.
### Create
This task is responsible for creating a new bulletin for a service.
##### Options
* **Service**. This is a mandatory input for this workflow operation. It is required to determine under which service the bulletin will be created. If this input is not provided, the operation will fail. When configuring this input, the manual option provides a list of services. When a service is selected, the ID of that service is passed as the input value. If the Service input is configured using free text or a variable, make sure the value provided is the ID of an existing service, not the service name.
* **Title**. The title of the newly created bulletin. The title field has a maximum length of 255 characters. If a title longer than 255 characters is provided, the workflow will truncate the value and use only the first 255 characters.
* **Description**. The description of the new bulletin.
* **Display Bulletin Text**. (Yes|No). Option to display the title and description text on the bulletin.
* **Display Bulletin Text Shadow**. (Yes|No). Display the bulletin text title with a shadow. This only applies if the "Display Bulletin Text" option is set to `Yes`. 
* **Visibility Start**. The start time of the bulletin. Make sure to provide a valid date format for this input. Providing an incorrect date value will cause the workflow operation to fail, and the bulletin will not be created.
* **Visibility End**. The end time of the bulletin. Make sure to provide a valid date format for this input. Providing an incorrect date value will cause the workflow operation to fail, and the bulletin will not be created.
* **Employee Portal Link**. A link used when viewing the bulletin in the employee portal. This field has a maximum length of 255 characters. If a link longer than 255 characters is provided, the workflow operation will not set any link for the bulletin.
* **Status**. The bulletin status (draft|publish|retire). The default value is draft. If no status is provided, or if the provided status is different from publish/published or retire/retired, the status is automatically set to draft.
* **Language**. The bulletin language. Defaults to en-GB. To use a different language, specify a language code supported by your instance, for example, de or fr.
The manual option shows a list of all supported languages in the instance. When a language is selected, its language code is passed as the input value.
If the input is configured using a variable, make sure to pass a supported language code. Passing an invalid language code will cause the workflow operation to fail, and the bulletin will not be created. Passing a valid but unsupported language code will make the bulletin inaccessible until that language is supported in the instance.
* **Create Default English Version**. Creates a default English version of the bulletin. This option applies only if the bulletin is created in a language other than English.

##### Outputs
* **Bulletin ID**. The ID of the created bulletin.
* **Outcome**. The operation outcome (success | failure).

### Delete
This workflow operation is responsible for deleting a bulletin.
##### Options
* **Bulletin**. This is a mandatory input for this workflow operation. It is required to determine which bulletin will be deleted. When configuring this input, the manual option provides a list of default bulletins. When a bulletin is selected, its ID is passed as the input value. If the Bulletin input is configured using free text or a variable, make sure the value provided is a valid bulletin ID. If the provided bulletin ID belongs to the default bulletin (to which all translations are linked), this workflow operation deletes the default bulletin and all its translations.
If the provided bulletin ID belongs to a translated version, only that specific translation is deleted.

##### Outputs
* **Outcome**. The operation outcome (success | failure).

### Update
This workflow operation is responsible for updating an existing bulletin.

##### Options
* **Bulletin**. This is a mandatory input for this workflow operation. It is required to determine which bulletin will be updated. When configuring this input, the manual option provides a list of default bulletins. When a bulletin is selected, its ID is passed as the input value. If the Bulletin input is configured using free text or a variable, make sure the value provided is a valid bulletin ID.
* **Title**. The new title for the bulletin. The title field has a maximum length of 255 characters. If a title longer than 255 characters is provided, the workflow will truncate the value and use only the first 255 characters. If this input is set to Auto or Ignore, the bulletin title will not be changed.
* **Description**. The new description for the bulletin. If this input is set to Auto or Ignore, the description will not be changed.
* **Display Bulletin Text**. (Yes|No). Option to display the title and description text. If this input is set to Auto or Ignore, the value will not be changed.
* **Display Bulletin Text Shadow**. (Yes|No). Option to display the bulletin text title shadow. If this input is set to Auto or Ignore, the value will not be changed.
* **Visibility Start**. The start time of the bulletin. Make sure to provide a valid date format. Providing an incorrect date value will cause the workflow operation to fail. If this input is set to Auto or Ignore, the Visibility Start value will not be changed.
* **Visibility End**. The end time of the bulletin. Make sure to provide a valid date format. Providing an incorrect date value will cause the workflow operation to fail.
If this input is set to Auto or Ignore, the Visibility End value will not be changed.
* **Employee Portal Link**. A link used when viewing the bulletin in the employee portal. This field has a maximum length of 255 characters. If this input is set to Auto or Ignore, or if the provided value exceeds 255 characters, the link will not be updated.
* **Status**. (draft|publish|retire). Change the status of the bulletin. If no status is provided, or if the provided status is not one of publish/published, retire/retired, or draft, the status will not be updated.
* **Language**. The bulletin language. Defaults to en-GB. To use a different language, specify a language code supported by your instance, for example, de or fr.
The manual option shows a list of all supported languages in the instance. When a language is selected, its language code is passed as the input value.
If the input is configured using a variable, make sure to pass a supported language code. Passing an invalid language code will cause the workflow operation to fail, and the bulletin will not be updated.
Passing a valid but unsupported language code will make the bulletin inaccessible until that language is supported in the instance.

##### Outputs
* **Outcome**. The operation outcome (success|failure).

## Update related services
### Status
The service status can help both the support staff and users on the portals to identify when a service is impacted or unavailable. The changes in service status can also contribute to the service [availability metrics](/service-portfolio/services/service-availability#availability-metrics).

##### Options
* **Request ID**. This is a mandatory option, but in most cases it should be set to `Auto`, which automatically picks up the request ID from the request that the workflow is running on.
* **Relationship Type**. This option sets the status update based on the dependency between the request's service and that service's dependencies. The default is set to `Ignore`, which will apply the status change to all services, independent of the dependency. The dependency options include:
    * Related and Request Service depend on each other
    * Request Service depends on Related
    * Related depends on Request Service
* **Related Services Type**. Select if the status update will apply to Business, Technical, or both Business and Technical services.
* **Status**. This is a mandatory option.  This needs to be set to `Manual`, and then one of the available statuses needs to be selected.

:::tip
The related services do not need to be added as a related service on the request for the status to be updated.
:::
