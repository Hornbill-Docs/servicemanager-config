---
layout: article-toc
---
# Application Settings
You can configure the various application settings associated with Hornbill Service Manager in **Configuration > Service Manager > Advanced Tools and Settings > Application Settings**. 

This document describes some of the more commonly used settings. This is not a complete list.

## Before you begin
* You must have the [Service Desk Admin role](/servicemanager-config/setup/service-manager-roles#administration-roles) or Hornbill Admin role to access the Service Manager settings.
* Be familiar with how to use [Configuration](/esp-config/getting-started/using-configuration).

## Topics covered
* [Accessing Application Settings](/servicemanager-config/advanced-tools-and-settings/application-settings#accessing-application-settings)
* [Using filters](/servicemanager-config/advanced-tools-and-settings/application-settings#using-filters)
* [Email settings](/servicemanager-config/advanced-tools-and-settings/application-settings#email-settings)
* [Category settings](/servicemanager-config/advanced-tools-and-settings/application-settings#category-settings)
* [Portal settings](/servicemanager-config/advanced-tools-and-settings/application-settings#portal-settings)
* [Intelligent Capture settings](/servicemanager-config/advanced-tools-and-settings/application-settings#intelligent-capture-settings)
* [Request list settings](/servicemanager-config/advanced-tools-and-settings/application-settings#request-list-settings)
* [Request settings](/servicemanager-config/advanced-tools-and-settings/application-settings#request-settings)
* [Knowledge Center settings](/servicemanager-config/advanced-tools-and-settings/application-settings#knowledge-center-settings)
* [Timeline settings](/servicemanager-config/advanced-tools-and-settings/application-settings#timeline-settings)
* [Configuration management settings](/servicemanager-config/advanced-tools-and-settings/application-settings#configuration-management-settings)

## Accessing Application Settings

You install Hornbill apps from the Hornbill App Store, which you access through Configuration.

**To access the Hornbill App Store:**
1. Open Configuration using the cog at the bottom of the left-hand menu bar (or with CTRL+SHIFT+S on your keyboard).
1. Click the down arrow next to *My Personal Settings*, then select **Service Manager**.
1. In the navigation panel, scroll down to *Advanced Tools & Settings*.
1. Select **Application Settings**.

## Using filters
At the top of the settings list, there are some options available to help you find the  settings you are looking for.

![Advanced Settings](/_books/servicemanager-config/advanced-tools-and-settings/images/include-advanced-settings.png)

Because advanced settings are less frequently used and potentially more complex to change, by default, they are not displayed in the list. If you are unable to find a particular setting, you may find that it is classed as an advanced setting. Select **Include advanced settings** to make sure even less frequently used settings are visible in the list.

## Email settings
### Archiving emails
Shared mailboxes can be configured to automatically move the email into a folder of your choice.

`servicemanager.email.archive`
* The default setting for this is `ON`. 
* When this setting is set to `OFF`, the email will remain in its current folder and the `archiveFolderName` setting will be ignored.

`servicemanager.email.archiveFolderName`
* The default folder name for this is `Deleted Items`. 
* This setting applies to all shared mailboxes that Service Manager users have access to.

### Email authorization
An email can be sent to a user that is assigned an authorization task. To receive and process the email authorization, the user must be a full user (not a Basic user).

`app.request.sendEmailToAuthorizers`
* The default setting for this is `OFF`. 

`guest.app.authorizations.email.revealOutcomes`
* The default setting for this is `ON`.
* When set to `ON`, an option to accept or reject the authorization is included as part of the authorization email. 
* Turning this setting to `OFF` removes the accept/reject option. The user will only have the option to click a link to view the authorization in Hornbill.

## Category settings
`servicemanager.request.closureCategory.default.enabled`
* The default setting for this is `OFF`.
* When this setting is `ON`, the resolution category is mandatory for all requests.
* If there are no defined closure categories, this setting is ignored.

## Portal settings
`guest.servicemanager.customer.request.showHistoricUpdates`
* The default setting for this is `OFF`.
* When this setting is `ON`, users of the Customer Portal will be able to see an additional collapsible panel on their Requests view that contains any related historical request-update data that may have been imported from a previous service management tool. This section is only visible on imported requests.

`guest.servicemanager.portal.request.showHistoricUpdates`
* The default setting for this is `OFF`.
* When this setting is `ON`, users of the Employee Portal will be able to see an additional collapsible panel on their requests view that contains any related historical request-update data that may have been imported from a previous service management tool. This section is only visible on imported requests.

`servicemanager.portal.requests.showStaffRequests`
- The default setting for this is `OFF`.
- When this setting is `ON`, managers are able to view requests raised by their direct staff via the Employee Portal. (The manager is the named user who is populated in the Manager field on a user's profile.)

`guest.servicemanager.portal.request.enableServiceRequestCancellation`
- The default setting for this is `OFF`.
- When this setting is `ON`, users of the Customer Portal will be able to cancel their service requests if no longer needed.
- The owner or team of the service request can receive an email, a Hornbill notification --- or both --- informing them of the cancellation.
- Customers must be assigned the [Self Service Request Cancel User role](/servicemanager-api-api/roles/content/selfservicerequestcanceluser) in order to use this feature.

`guest.servicemanager.customer.request.enableServiceRequestCancellation`
- The default setting is `OFF`.
- When the setting is `ON`, guests are able to cancel their service requests from within the Customer Portal.
- The owner or team of the service request can receive an email, a Hornbill notification --- or both --- informing them of the cancellation.
- Customers must be enabled to use this feature via the Portal Access option available in Organization > Details > Request tab.

    **To enable this cancellation feature:**
    1. When viewing the details of an organization, scroll down and expand the Requests section. 
    1. At the top right, click **Portal Access**.
    1. In the Customer Portal Access dialog, toggle settings for portal users as needed.

`guest.servicemanager.portal.additionalRequestTypes.change`
- The default is `OFF`.
- When this setting is `OFF`, customers cannot see changes on the portals' requests lists, nor can they see any configured portal-visible change catalog items.
- When this setting is `ON`, customers can see all new and historic change records in the request lists on the portals where they are the marked as the customer.
- When this setting is `ON`, customers have the option to see and use portal-visible change catalog items for their subscribed services.

`guest.com.hornbill.servicemanager.showRespondByDate`
- The default is `OFF`.
- When this setting is `ON`, the respond by date/time is displayed in the right-hand information box of a request when viewed by a user on the Employee Portal or a customer on the Customer Portal.

`guest.com.hornbill.servicemanager.showResolveByDate`
- The default is `OFF`
- When this setting is `ON`, the resolve by date/time is displayed in the right-hand information box of a request when viewed by a user on the Employee Portal or a customer on the Customer Portal.

## Intelligent Capture settings

### Service Manager forms

**Only show supported and subscribed services** `servicemanager.progressiveCapture.servicedetails.enableSupportVisibility`
- The default setting for this is `OFF`.
- When this setting is `ON`, the services displayed on the [Services form](/servicemanager-config/customize/service-manager-capture-forms#services) are filtered to both those which the customer is subscribed to, and also to those services which the Service Manager user supports.

**Only show supported requests** `app.itsm.progressiveCapture.customerDetails.showOnlySupportedRequests`
- The default setting for this is `OFF`.
- This setting determines whether a Service Manager user is granted visibility to unsupported customer requests in the *Customer Search*, *Contact Search*, or *Co-worker Search* forms in Intelligent Capture.
- When set to `OFF`, a Service Manager user has visibility to unsupported customer requests. This should be set to `ON` in environments with multiple service desks (e.g. IT and HR).

**Show all requests for an external organization** `app.itsm.progressiveCapture.organizationDetails.allowOrgRequestsList`
- The default setting for this is `OFF`.
- When this setting is `ON`, the analyst viewing the [Organization Details form](/servicemanager-config/customize/service-manager-capture-forms#organization-details), can see the active requests for the organization in the right-hand panel.
- The requests returned are active ones, and only the requests raised against services that the viewing user supports are displayed.

### Visibility of a request's *Questions* section
The following settings influence how information from [customized forms](/servicemanager-config/customize/customized-forms) in Intelligent Capture are made available within the *Questions* section of a request.

**Hide unanswered questions in the Service Manager app** `app.request.questions.hideUnansweredQuestions`
- The default setting for this is `OFF`.
- Fields on a customized form in Intelligent Capture can be set specifying whether they require a value or if a value is optional. If a value is not required, a user can move on without providing a response.
- When this setting is `ON`, any unanswered fields from custom forms used in Intelligent Capture will not be displayed in the *Questions* section of a request.

**Hide unanswered questions on the Customer Portal** `guest.servicemanager.customer.request.questions.hideUnansweredQuestions`
- The default setting for this is `OFF`.
- When this setting is `ON`, unanswered fields in the *Questions* section of a request are hidden from contacts in the Customer Portal.

**Hide unanswered questions on the Employee Portal** `guest.servicemanager.portal.request.questions.hideUnansweredQuestions`
- The default setting for this is `OFF`.
- When this setting is `ON`, unanswered fields in the *Questions* section of a request are hidden from users in the Employee Portal.

**Hide unused conditional questions** `app.request.questions.excludeConditionalQuestions`
- The default setting for this is `OFF`.
- When designing an Intelligent Capture script, a user may find that some fields on a customized form are displayed only under certain conditions.
- When this setting is `ON`, conditional questions that are not displayed to the user are prevented from being stored in the *Questions* section of a request.

**Hide questions that are not visible on forms** `guest.request.questions.excludeHiddenQuestions`
- The default setting for this is `OFF`.
- On a Customized Capture form, each field has an option to make it visible. 
- When this setting is `ON`, fields on customized forms that are not set to being visible are excluded from the *Questions* section of a request, when viewed from either the Customer or Employee Portal.
- When this setting is `ON`, all questions are still visible on the *Questions* section when viewed in the Service Manager app.
- When this setting is `ON`, all fields are still added to the `h_itsm_questions` table. This enables hidden questions with default values to still be utilized in a workflowBPM.

## Request list settings
`com.hornbill.servicemanager.requestList.restrictions.service`
- The default setting for this is `ON`.
- When this setting is `ON`, it is only possible to perform multi-select actions against requests logged against the same service. When selecting requests logged against different services, the multi-select action buttons are hidden.
- When this setting is `OFF`, it is possible to perform multi-select actions against requests logged against different services.

`com.hornbill.servicemanager.requestList.restrictions.type`
- The default setting for this is `ON`.
- When this setting is `ON`, it is only possible to perform multi-select actions against requests of the same type. When selecting requests of different types, the multi-select action buttons are hidden.
- When this setting is `OFF`, it is possible to perform multi-select actions against requests of any types.

    ::: note
    When the multi-select restrictions are `OFF`, the supporting-teams logic is disabled on the Assign option on the request list, making it possible to assign requests to teams that are not listed as supporting the services requests are logged against.
    :::

`webapp.view.ITSM.serviceDesk.requests.list.enableNoTeamAllUsers`
- The default setting for this is `OFF`.
- When this setting is `ON`, it is possible for ANY Service Manager subscriber to see any requests that are not assigned to any team.
- When this setting is `OFF`, it is only possible for Service Manager subscribers with the Service Desk Admin role to see any requests that are not assigned to any team.

## Request settings

`app.request.questions.excludeConditionalQuestions`
- The default setting for this is `OFF`.
- When this setting is `OFF`, conditional Intelligent Capture questions that were not displayed in Intelligent Capture flows will appear in the *Questions* section on the request forms.
- When this setting is `ON`, conditional Intelligent Capture questions that were not displayed in Intelligent Capture flows will not appear in the *Questions* section on the request forms.

## Knowledge Center settings
This feature allows agents and customers to be presented with relevant knowledge when using Intelligent Capture in the user app and the Customer and Employee Portals,respectively.

`guest.app.experimental.hornbillKnowledgeCentre`
- The default setting for this is `OFF`.
- When this setting is `ON`, you must also set which interfaces will see the Knowledge Center in Intelligent Capture. This is controlled by the following system settings:

    `guest.app.knowledge.customer`
    * The default setting for this is `OFF`.
    * When this setting is `ON`, the relevant knowledge is shown when a user logs a new request in the Customer Portal.

    `guest.app.knowledge.service`
    * The default setting for this is `OFF`.
    * When this setting is `ON`, the relevant knowledge is shown when a user logs a new request in the Employee portal.

    `guest.app.knowledge.user`
    * The default setting for this is `OFF`.
    * When this setting is `ON`, the relevant knowledge is shown when a user logs a new request in the user app.

## Timeline settings

`guest.servicemanager.request.timeline.showShortPostTitle`
- The default setting for this is `ON`.
- When this setting is `ON`, the name of the user who posted on the timeline of the request will be displayed when the timeline of the request is viewed in the Customer and Employee Portals.
- When this setting is `OFF`, the name of the user who performed the post can still be viewed by hovering over the image of the user on each post.

`servicemanager.request.timeline.showShortPostTitle`
- The default setting for this is `ON`.
- When this setting is `ON`, the name of the user who posted on the timeline of the request in the user app will be displayed when the timeline of the request is viewed.
- When this setting is `OFF`, the name of the user who performed the post can still be viewed by hovering over the image of the user on each post.

`guest.servicemanager.request.timeline.availablePostTypes.editPost`
- This setting determines the type of posts that a user is allowed to edit. Selecting additional post types allows a user to edit their own post in a timeline, provided that the post has not been liked or commented on.
- The default setting for this is `NONE`; that is, the option to edit a post is disabled.

## Configuration management settings

`app.cm.explorer.diagram.expand`

These are the entities that can be expanded in the Explorer. The entities with `false` will have no icon to expand/collapse. If a new entity is added in the future, and this object is not updated with the new entity name, then its value will be set to the default value, which is `false` (i.e. the user will not be able to expand/collapse the nodes for that entity).

The entities currently shown in the diagram are Asset, Colleagues, Contact, Attachment, Requests, Services.

**Default settings:**
* Asset: `true`
* Colleagues: `false`
* Contact: `false`
* Attachment: `false`
* Requests: `true`
* Services: `true`
* default: `false`

`app.cm.explorer.diagram.level.max`
* The maximum level shown in the Explorer. The minimum value is 2 (root plus children).
* The default is `3`.

`app.cm.explorer.items.dependencies`
* This setting holds the possible dependencies that can be set between two entities. 
* The possible entities are Asset, Colleagues, Contact, Attachment, Requests, and Services. The property definitions hold all possible lists of values.

**To associate a list to two linked entities:**
1. Add a property by following this rule:

    From + entity1 + To + entity2, where entity1 and entity2 can be any value chosen from Asset, Colleagues, Contact, Attachment, Requests, or Services. If the two entities are the same (e.g., two assets), then you may define the list of possible values as `AssetFromParentToChild` and `AssetFromChildToParent`.
    
    This works the same way for other entities. Any missing value will default to the list in `defs.default`.

    >"defs" : {<br>
"set1" : ["Connected To", "Depends On", "Installed On"],<br>
"set2" : ["Connected To", "Depends On", "Installed On"],<br>
"default" : ["Connected To", "Depends On", "Installed On"]<br>
         }<br>
"FromAssetToRequests" : "set1",<br>
"FromRequestsToAsset" : "set2",<br>
"FromAssetToServices" : "set2",<br>
"AssetFromParentToChild" : "set2",<br>
"AssetFromChildToParent" : "set2"<br>
app.cm.explorer.items.inPolicy<br>
{{{2}}}<br>
"Asset" : true,<br>
"Colleagues" : true,<br>
"Contact" : true,<br>
"Attachment" : true,<br>
"Requests" : true,<br>
"Services" : true,<br>
"default" : true<br>

<!--https://wiki.hornbill.com/index.php?title=Service_Manager_Settings>
<!-- https://wiki.hornbill.com/index.php?title=Service_Manager_Experimental_Features -->