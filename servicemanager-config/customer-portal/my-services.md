# My Services

Service Manager provides a My Services app for [contacts](/esp-config/guest-access/contacts) that are external to your organization, which is accessible through the [Customer Portal](/esp-config/customize/customer-portal/configure-customer-portal).

The My Services app is a window into the Service Desk, with the ability for the Service Desk teams to publish everything from bulletins to FAQs, service subscriptions, known issues, and communications about the progress of the requests raised by or for the customers.

![Service Manager Self-service](/_books/servicemanager-config/images/customer-portal-self-service-app.png)

## Services
The services are centric to supporting customers and to providing information and ways of raising requests on the Service Manager self-Service app. Customers get visibility of the services that they are subscribed to and are able to access the ability to raise requests, view bulletins, be made aware of the status of a service, and much more.

### Subscribed Services
Customers using the service and or Customer Portal will only see services to which they are subscribed.
* When a new service is configured, the default position is for all customers to be automatically subscribed.
* Manage subscriptions to services via the service portfolio.

### Service Navigation
When accessing the Service and or Customer Portals, customers will be presented with a navigation control. Default behavior will only show the navigation options, if the customer has selected Favorite Services, has active requests raised against a service or is subscribed to services which are marked as impacted.

* **Favorites**. This will show all services that an individual customer has marked as being one of their favorites. Favorites can be set by clicking on the heart icon on the Service details or under the More option of each Service.
* **Active**. This will show the customer a view of any service for which the customer currently has active requests.
* **Impacted**. This will show the customer a view of any service which have been marked as impacted or degraded.
* **All Services**. This will show the customer a view of all the services they are subscribed to.
* **Service Categories**. Use the drop-down to filter the displayed services to those of a specific category of service. The list will only show the categories where the user is subscribed to a service in that category. The categories are managed in the admin tool > Simple Lists, and can be associated with each service, in the service details section of the Services view.

### Service Bulletins
Service owners can publish one or multiple announcements to the subscribed users of their Service.. When bulletins are marked as published, any subscribed user of the service against which the bulletin has been published will be able to view the bulletin on the Customer and Service Portal in two locations.

* **My Services View**. If multiple bulletins have been published from either the same or different Services a User is subscribed to, they will view the bulletins in a carousel at the top of the My Services view.
    * Click on the bulletin details, or the service name to be taken to the Service View that the bulletin relates to.
    * Clicking on any hyperlink in the Bulletin text will open the link in a new browser tab.
* **Service Specific Details View**. If one or multiple bulletins have been published from the same Service, they will appear in thhe service specific view. Again, if there are multiple bulletins, these will appear in a carousel.
    * Clicking on any hyperlink in the bulletin text will open the link in a new browser tab.

:::tip
If multiple bulletins are published, they will automatically transition through the carousel every 5 seconds, if not manually progressed using the Arrow controls on the carousel. 
:::

### Service Details
Each Service will display its name, a configurable icon, and a description for the service. By expanding the `More` option against each service, a more detailed view is presented.

* Full service description.
* Option to make the service a favorite by selecting the Heart icon.
* Option to open the display details.
* Options to raise an incident and or service request (depending on what has been configured against the service).
* View of the total number of active requests the customer has against the Service, with the ability to drill down into the list of these requests.

If the customer has any active requests for a service, this will be represented by a numerical value.
* If the status of the service has been set, this will be represented with an icon and color - hovering over the impact icon will provide more information.
* Drill down into the Service Details from the service Icon.

## Requests
### Reporting an Issue or raising a service request
As a subscribed customer to a service, it is possible to make a request against each service. The service owner will have configured their service to either allow requests to be raised against each Service, or not. A customer can access these options from two places:
* By expanding the More option on the relevant Service, select the Make a Request option to be taken to the Request Catalog.
* By drilling into the service details through the service icon and viewing the "Make a Request tab."

By selecting the appropriate option, the customer will be guided through a series of questions to gather the information about their issue or request using an intuitive intelligent capture. The questions can be configured by the service owner using the Inteligent Capture Designer. Here, they can use a combination of default question forms and custom question forms with branching to define the different data capture requirements for each service, and request type.

### Viewing and Updating Requests
Customers can view the requests they have raised against each of their Services (irrespective of how they were logged) by using the `All My Requests` navigation option on the home page, or by drilling down into each service, to see service specific requests . If a customer has active requests against a given Service, this will be indicated by a numerical value on the Services home page, and or by switching the view to Active.

By drilling into a Service, a customer will be presented with a list of their active requests and a filter option to switch to their historical closed requests.

#### Viewing Requests
* Customers can view the progress of their requests graphically via the process tracker display. This represents the fulfillment process stages and checkpoints. Each service owner can define if the process tracker is shown, if it only shows stages, or if it shows stages and checkpoints.
* Request resolution targets can be made visible by enabling the guest.com.hornbill.servicemanager.showResolveByDate setting in the Administration console - Home > Service Manager > Settings
* Customers will have access to the request timeline, which shows all customer facing updates to the request.
* Customers can see any attachments to the request that have been marked as customer facing
* If any custom questions have been asked during the logging process of the request, these are visible to the customer.
* Request and ownership details are visible.

#### Viewing all company requests
It is possible to elevate an individual contact's access, to not only view their own requests on the Customer Portal, but also to see all the requests raised by other contacts from the same company.

* From a company record, expand the **Requests**  section.
* Click on `Portal Access` to configure which contacts can access all company requests.
* From the pop-up window toggle on or off the `Company View`.

#### Updating a Request
* Customers can post an update on the request.
* Customers can provide a comment against an existing post in the timeline - this will make it easier for the analysts working on the request to understand the context of the update and what it relates to.
* Customers can cut and paste images and share video content into a post or comment (Browser permitting).
* Customers can upload attachments.
* Customers can view and watch videos inline in the timeline if these have been shared with them.

#### Accepting a proposed resolution
When a request is in a resolved status, a customer can review the proposed resolution.

* Customers can mark a resolution as *It's working* which can automatically close the request.
* Customers can mark a resolution as *It's still broken* which can change the status from resolved to open.

#### Customer Feedback
If a request is in a closed status, a customer can provide feedback on the level of support they have received. Customers will see if they have any requests awaiting feedback from their request list, Awaiting Feedback.

Customers can choose to provide feedback, save for later, or say *No Thanks* and not provide feedback. 

#### Canceling a Service Request

Customers can be given the right to cancel service requests if they are no longer needed. When viewing a service request a customer can select the cancel option and provide a reason for the canceling of the request before submitting. The owner or team responsible for the request can receive a notification of the cancelation. Read more about enabling this feature here under Portal Settings and configuring the Notification Settings.

## Request Catalog
Subscribed users of a service can view and select what type of request they would like to raise from the Request Catalog.

* The default options will be Get Help or Raise a Request, but the Service owner can configure the different Catalog options they wish to present per service by configuring the Request Catalog
* Users can select the relevant Catalog option and be guided through linked questions to submit the request.
* The Service Owner will have configured in the request catalog whether the request will be raised as an incident or a service request against each Catalog item.

If The Raise Request tab is not visible this will be because no catalog items have been defined and the Service Owner may not want to allow subscribed users to be able to raise requests against the Service from the Portal, however they may still want them to review their requests raised via other channels for the Service, and or view or have access to 
FAQs' about the Service.

## FAQ's
Subscribed users of a service can view all the published FAQ's for a service via the Customer and Service Portals. Click through to the details of each Service to see the FAQ tab.

* The FAQ questions are presented, and the answers can be displayed by expanding the collapsed sections.
    * Media content can be viewed in line
    * Hyperlinks will behave as configured when added to the answer text by the FAQ creator (open in new tab, etc.)
* Each view of the FAQ is automatically recorded.
* Users can rate the FAQ as being useful (Like) or not (Dislike) through the thumps up or down options.
    * All ratings are recorded and are visible both on the FAQ for other users to see how their colleagues rated the FAQ, and on the FAQ tab of the Service record for the Service Owner to review
* Create FAQ's

## Known Issues
Subscribed users of a service can view any existing known issues that relate to the Service.

Problems and Known Errors can be published to the portals, to keep users informed of ongoing issues, and where appropriate, communicate workaround information. In doing so, this reduces the number of repeat Incidents for known issues.

* In addition to being made aware of a known issue, a user can also opt to link themselves as an Impacted user to the Problem or Known Error by selecting the Me Too button. This will add the user as a Connection to the Problem or Known Error and the Problem team will see the real impact of the Problem or Known Error with the end users.
* The Problem Management Team can use the business process engine to automatically keep Affected Connections informed of progress or on the resolution of the issue via email.
Known issues can be published selectively by the Problem management team.
* The list of Known issues is displayed in an order that shows the newest or most recent issues first. A user can change the order to show the oldest requests at the top of the list by using the order option. Order options include Newest and Oldest.

## Search

The Search option of the Self Service Portal provides a starting point for anyone not knowing where to navigate to raise their request or find information, but they don't know which Service it is stored under.

The Search provides results in the following areas

* Requests
* Services
* FAQs
* Known Issue
* Request Catalogs

### Suggested Search Terms
Each time a user enters text in the search box and performs a search, the search term is saved in the database and can be reported on, for you to better understand what content users are looking for and to assist you in knowing where more information is needed, and this could be provided by the creation of relevant FAQs.

Suggested Search Terms - Users will be presented as they type with relevant search terms which they have previously used, or other users have used, where they share the same services.