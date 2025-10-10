---
layout: article-toc
---
# Service Manager Forms
Service Manager provides several default forms that are available to use when building an Intelligent Capture script. These forms can be made available to an Intelligent Capture script by adding a form node to your Intelligent Capture and selecting the form name from within the properties of the node.

## Before You Begin
* Become familiar with the [Intelligent Capture designer](/esp-config/automation/intelligent-capture-designer).

## Add Attachments
The Add Attachments form allows you to include files when raising a request. Multiple attachments can be added and individual descriptions can be applied to each. 
* Add attachments such as screenshots while raising a request.
* Browse your local file system or drag and drop files.
* Includes description of attachment for easy reference.
* Stores attachments in the Attachments section of a request for easy access.

### Options
* Specify a custom title on the form.
* Specify a custom information message to describe to the user the type of attachment that you are requesting. This option can contain wiki formatting for improved presentation.
* Hide the past input field. 
:::tip
Attachments are regulated by the following system settings that restrict size and type:
* maxfileUploadSize
* security.fileUploadRestriction.webdav.enable
* security.fileUploadRestriction.entity.fileAttachments.types
:::

:::tip
More than one attachment form can be included within a single Intelligent Capture workflow. Any subsequent attachment form needs to be set to mandatory for the Intelligent Capture to stop and prompt the user on that form.
:::

## Assignment
The Assignment form provides options for assigning the request to a team and an individual who will own the request. You can choose to assign the request to just a team or to a team and an owner.
* Search for Team and Owner to assign the request to.
* When preceded by the Service Details Form, only teams that support that service will be displayed.
* Only visible to service desk users.
* Branch nodes that follow this will be able to use Team Name, Team ID, Analyst Name, and Analyst ID as criteria for branching.

### Options
* **Owner is mandatory**<br>When set to `Yes`, the owner or analyst field becomes mandatory and must be selected to continue. 

## Assets
The Asset form allows an analyst or customer to associate assets with a request. By default, all assets that are associated with the customer are shown; however, it is also possible to associate assets that are shared with the customer, or perform general searches on assets that reside at the customer site, or more widely in the system. It is possible to associate multiple assets to each request.

* View assets owned and used directly by a customer.
* View assets shared with a customer (directly or via their membership to groups or organizations the asset has been shared with).
* Search assets by site or more widely.
* Input: Following a Search Co-worker/Contact or Customer form, the assets belonging to or shared with the customer will be displayed.
* Visibility: Analysts and Customers.
* Branch Options: None.
* If this node is preceded by the Sites node, the Sites tab will be automatically filtered to only display assets located at the selected site.

### Options
* **Asset Title**<br>Displays a title at the top of the Asset form.
* **Info Message**<br>Add a longer descriptive message explaining to the user how to use the form.
* **Hide Customer's Assets**<br>Select `Yes` to always have this tab hidden.
* **Hide Shared Assets**<br>Select `Yes` to always have this tab hidden.
* **Hide Customer's Site Assets**<br>Select `Yes` to always have this tab hidden.
* **Hide Company Assets**<br>Select `Yes` to always have this tab hidden.
* **Hide All Assets**<br>Select `Yes` to always have this tab hidden.
* **Hide Service Assets**<br>Select `Yes` to always have this tab hidden.
* **Select Asset Class**<br>On the Asset Search, set the Asset Class to be searched.
* **Select Asset Type**<br>On the Asset Search, set the Asset Type to be searched.
* **Select Asset Status**<br>On the Asset Search, set the Asset Status to be searched.
* **Select Asset Relationship**<br>Specify the default asset relationship that will be the focus of the asset search.
* **Asset Search Term**<br>On the Asset Search, set a default search term to be searched.
* **Select Asset Search Type**<br>On the Asset Search, specify whether the results return assets with an exact match of, *contains*, or *begins with* the specified search term.

:::note
The "Select Asset ..." parameters only affect tabs that search for assets. The customer's Assets and Shared Assets tabs will show all Assets that are Owned By or Shared With the customer respectively.
:::

### Asset Data Query on a Custom Form
As an alternative to the full asset form, you can add a field to a [Custom Form](/esp-config/automation/customized-forms) that uses a data query to present assets in a dynamic drop-down select box, radio set, or check-box group.

* **Get All Assets**. All assets are available to select from.
* **Get All Assets by Type**. Only display assets that are of a particular type.
* **Get All Assets by Class**. Only display assets that are of a particular class.

![Asset Data Query](/_books/servicemanager-config/images/capture-asset-data-query.png)

* **Filter Assets**. Assets will only be visible if the asset ID contains the filter text.
* **Include Archived Assets**.  Including archived assets is set to **Yes** by default.  Set this to **No** to hide archived assets.

## Categories
The Category form will display the request category profile structure to the user.  The category used will be based on the category root specified on the request type configuration on the Service details form.  When a category is selected, the [description of the category](/esp-config/data/profiles#editor) will be displayed to the user.
* Request Category selector.
* When preceded by the Service Details form, the category will display the configured root category for the selected service.
* Use the Mandatory option to force a user to pick a category before exiting the form.
* If you want to ensure the user chooses a category from the lowest level of the available category tree structure, ensure the following system setting is enabled: guest.servicemanager.request.category.request.enforceLastItem.


## Change Type
The Change Type form allows an analyst to select the type of change request that will be raised. This form is usually only seen on the new Change capture flow:
* **Select Change Type**

## Connections
The Connections form allows the support person to select a connected customer at the time of raising a request. This form is only used by and visible to support staff when raising the request in Service Manager when using the full client.

![Connection Capture form](/_books/servicemanager-config/images/capture-connections.png)

* **Connection Search**<br>Search for one or more customers that you would like to add as a connection to the request.
* **Connection Type**<br>A pick list of available connection types is available to allow you to select the type of connection being added.

See the [Connections configuration](/servicemanager-user-guide/service-portfolio/services/service-connections) on a service for more information about connections.

## Customer Search
The Customer Search form allows an analyst to select a customer for the request. This search returns both contacts and co-workers. This form is useful when a support team is supporting both external and internal customers.

![Customer Search Form](/_books/servicemanager-config/images/capture-customer-search-form.png)

* Search on both contacts and co-workers.
* Filter on contacts or co-workers.
* The customer's details and active requests are displayed after a customer is selected.

:::important
This form will not be displayed on the Employee or Customer portals. 
:::
<br>

#### Advanced filtering
By appending one or more of the following keys, you can narrow the search to specific areas:
* **org:** This filters by organization.
* **site:** This filters by site.
* **type:** This filters by co-worker type (basic, user, or contact).
* **tel:** This filters by the primary telephone number.
* **phone:** This is equivalent to **tel:** and will also filter on the primary telephone number.<br>

**Example:** `Joe org:ACME` would return all customers named Joe from the ACME Organization<br>

#### Additional Display Fields
These can be used to display selected fields within the right-hand side of the Intelligent Capture during the capture process. When one or more fields are added, the default fields will no longer be displayed.  If this option is left blank, the following default fields will be displayed:
* Job Title
* Phone
* E-mail
* Mobile
* Feedback

### Customer Search Output
After this form has been completed, there are several variables that contain information about the selected customer.  These variables can be used as part of a custom expression in a decision node and for conditions on a custom form's override flag. These variables are prefixed with Customer Search.

![Customer Search Output](/_books/servicemanager-config/images/capture-customer-search-output.png)

:::tip
h_custom fields are stored on the contact record and h_attrib fields are from the user account.
:::
<br>

#### Advanced Settings

|Setting|Description|
|-|-|
|app.itsm.progressiveCapture.customerDetails.showOnlySupportedRequests|The list of the customer's requests can be filtered to only show those that the logging agent supports via the linked service: . When disabled, an agent will have visibility to unsupported customer requests.|
|app.itsm.progressiveCapture.customerSearch.allowAddContact|An option to add a new Contact can be displayed on this form when this setting is enabled.| 

## Contact Search
The Contact Search form provides a search option for adding a contact as the customer for the request. The search results only display contact records. Contact Search is recommended to use when only providing external support.
* Search all contacts.
* Configure fields to be displayed on the right-hand side.
* The Contact's active Requests are displayed when a contact is resolved.
    * The list of the contact's Requests can be filtered to only show those that the logging agent supports via the linked service: app.itsm.progressiveCapture.customerDetails.showOnlySupportedRequests. When disabled, an agent will have visibility to unsupported customer Requests; this must be avoided for customers with multiple service desks (e.g. IT and HR).
    * An option to add a new Contact can be displayed on this form if the following system setting is enabled: app.itsm.progressiveCapture.contactSearch.allowAddContact.

## Co-worker Search
The Co-worker Search form provides a search option for adding a Co-worker as the customer for the request. This search results only display co-worker records and is recommended to use when only providing internal support.
* Search all Co-workers.
* Configurable field to be displayed on the right-hand side.
* The Co-worker's active Requests are displayed when a co-worker is resolved. The list of the Co-worker's Requests can be filtered to only show those that the logging agent supports via the linked service: app.itsm.progressiveCapture.customerDetails.showOnlySupportedRequests. When disabled, an agent will have visibility to unsupported customer Requests, this must be avoided for customers with multiple service desks (e.g. IT and HR).

:::tip
The Co-worker Search includes an additional option to show archived users in the list that is presented to the user.  This can be useful when raising requests regarding people who may have left the company.  
:::

## Known Error Details 
The Known Error Details form allows an analyst to specify the root cause and workaround details for a known error. This form is usually only seen on the new Known Error Intelligent Capture script:
* Provide the root cause and workaround details.

## Organization Details
The Organization Details form allows an analyst to see additional information about the customer's organization that is defined by a Hornbill administrator. There is no data captured in this form; it is informational only.
* Display only.
* Will display the organization of a previously selected contact.
* Recommended use after the Contact Search.
* Configurable organization fields for the right-hand side.

## Release Type
The Release Type form allows an analyst to select the type of release request that will be raised. This form is usually only seen on the new Release Intelligent Capture Script:
* Select Release Type.

## Request Details
The Request Details form allows an analyst to enter both a summary and a description for the request.
* Add a summary to the request.
* Add a detailed description to the request.

## Request Priority
The Request Priority form allows the priority of the request to be set.
* Select the Priority for the request.

## Select Site
The Select Site form allows an analyst or customer to specify a site when logging a request:
* The All Sites filter allows you to search for a site by name.
* If preceded by the customer/co-worker form, this will show the option to pick the site associated to the customer.
* If a customer belongs to a Company internal organizational group, and that Company also has associated sites, then a Company site filter will appear and you can search for sites that are associated to the customers company.
* If preceded by the asset form, it will show the option to pick the site associated to any of the assets.
* Branch Options: The name of the selected site can be used in a branch node.

### Options
* **Limit Portal Search to Name**<br>If set to NO, the postcode and site ID are included in the search. If set to YES, then only the name of the site name is searched on.
* **Info Message**<br>Add a longer descriptive explaining to the user how to use the form.
* **Hide Customer's Site**<br>Select `Yes` to always have this tab hidden.
* **Hide Company Sites**<br>Select `Yes` to always have this tab hidden.
* **Hide Asset Sites**<br>Select `Yes` to always have this tab hidden.
* **Hide All Sites**<br>Select `Yes` to always have this tab hidden.
* **Hide All Sites in Portals** (if All Sites option is not hidden)<br>Select `Yes` to always have the Sites tab hidden when viewing on the portals.

## Services
The Services form allows a Service Manager user to select a service when capturing information during request creation.  Each service will also display their associated request catalog if available.
* Displays Request Catalog Items under each Service.
* If preceded by the Customer, Co-worker, or Contact Search, the Service Details will only show the subscribed services for the selected person.
* If preceded by the Requests Type form, only the Request Catalog Items that match that type will be displayed.
* Filter option by Service Category.
* Setting: servicemanager.progressiveCapture.servicedetails.enableSupportVisibility - restricts the view so that the list of services also only includes the services supported by the analyst.
* Setting: servicemanager.progressiveCapture.servicedetails.catalogRequired - enforces the selection of a request catalog item if one exists under a Service.

:::tip
This form will not be displayed to anyone raising requests through the Customer or Employee portals.
:::

### Form Features
* Filter services by name.
* Displays Request Catalog under each Service.
* If this form is preceded by the Customer, Co-worker, or Contact Search, the Service Details will only show the subscribed services for the selected person.
* If this form is preceded by the Request Type form, only the Request Catalog Items that match that type will be displayed.
* Filter option by Service Category.

### Branching
The name of the selected service can be used in a branch node that follows this node.

### Application Settings
The following settings can be use to change the behavior of the Services form.  These settings can be updated in the [Application Settings](/servicemanager-config/advanced-tools-and-settings/application-settings) for Service Manager.
|Name|Description|
|-|-|
|servicemanager.progressiveCapture.servicedetails.enableSupportVisibility|Restricts the view so that the list of services also only includes the services supported by the analyst.|
|servicemanager.progressiveCapture.servicedetails.catalogRequired|Enforces the selection of a request catalog item if one exists under a service.|



