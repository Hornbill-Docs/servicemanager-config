---
layout: article-toc
---
# Application Settings
The various application settings associated with Hornbill Service Manager can be configured in Configuration under the Service Manager app. This document describes some of the more commonly used settings. This is not a complete list and more settings can be viewed within Configuration.


## Accessing Application Settings

1. Select the Configuration Cog on the bottom of the left hand application menu bar
1. From the Configuration Selector choose Service Manager
1. Scroll the navigation panel and find the section Advanced Tools and Settings
1. Select Application Settings

## Email Settings
### Archiving Emails
The Shared Mailboxes can be configured to automatically move the email into a folder of your choice.

`servicemanager.email.archive`
* The default setting for this is 'ON'. 
* When this setting is set to 'OFF' the email will remain in its current folder and the archiveFolderName setting will be ignored.

`servicemanager.eamil.archiveFolderName`
* The default folder name for this is 'Deleted Items'. 
* This setting applies to all Shared Mailboxes that Service Manager Users have access to.

### Email Authorization
An email can be sent to a user that is assigned an authorization task. The user must be a full user and not a Basic user in order to receive and process the email authorization.

`app.request.sendEmailToAuthorizers`
* The default setting for this is OFF. 

`guest.app.authorizations.email.revealOutcomes`
* By default, an option to accept or reject the authorization is included as part of the authorization email. 
* Turning this setting off will remove this option and the user will only have the option to view the authorization.

## Category Settings
`servicemanager.request.closureCategory.default.enabled`
* The default setting for this is 'Off'.
* When this setting is 'On' the resolution category will be mandatory for all requests.
* If there are no defined Closure Categories, this setting is ignored.

## Portal Settings
`guest.servicemanager.customer.request.showHistoricUpdates`
* The default setting for this is 'Off'
* When this setting is 'On' users of the Customer Portal will be able to see an additional collapsible panel on their requests view, containing any historical request update data which may have been imported from a previous Service Management tool which relates to that request. This section will only be visible on imported requests.

`guest.servicemanager.portal.request.showHistoricUpdates`
* The default setting for this is 'Off'
* When this setting is 'On' users of the Service Portal will be able to see an additional collapsible panel on their requests view, containing any historical request update data which may have been imported from a previous Service Management tool which relates to that request. This section will only be visible on imported requests.

`guest.servicemanager.portal.request.questions.hideUnansweredQuestions`
- The default setting for this is 'Off'
- When the setting is 'On' any unanswered questions from custom forms used in progressive capture will not be displayed in the Questions section on Request forms in the Service Portal

`guest.servicemanager.customer.request.questions.hideUnansweredQuestions`
- The default setting for this is 'Off'
- When the setting is 'On' any unanswered questions from custom forms used in progressive capture will not be displayed in the Questions section on Request forms in the Customer Portal

`servicemanager.portal.requests.showStaffRequests`
- The default setting for this is 'Off'
- When the setting is 'On' Manager's will be able to view requests raised by their direct staff via the Service Portal.
- Manager refers to the named user who is populated in the Manager field in a staff user's profile.

`guest.servicemanager.portal.request.enableServiceRequestCancelation`
- The default setting for this is 'Off'
- When this setting is 'On' Customers on the Service Portal will be able to cancel their Service Requests if no longer needed.
- The Owner or Team of the Service Request can receive an email, Hornbill Notification or both informing them of the cancelation.
- Customers will also need to be assigned the Self Service Request Cancel User role in order to use this feature

`guest.servicemanager.customer.request.enableServiceRequestCancelation`
- The default setting is 'Off'
- When the setting is 'On' Contacts on the Customer Portal will be able to cancel their Service Requests if no longer needed.
- The Owner or Team of the Service Request can receive an email, Hornbill Notification or both informing them of the cancelation.
- Customers will need to be enabled to use this feature via the Portal Access option available under the Organization > Request tab

`guest.servicemanager.portal.additionalRequestTypes.change`
- The default is 'Off'
- When the setting is 'Off' customers will not see Changes on the portals requests lists, nor see any configured portal visible Change Catalog Items
- When the setting is 'On' customers will see All new and historic Change records in the request lists on the portals where they are the marked as the customer
- When the setting is 'On' customers will have the option to see and use portal visible change catalog Items for their subscribed services

`guest.com.hornbill.servicemanager.showRespondByDate`
- The default is `Off`
- When this setting is 'On' the Respond by date/time will be displayed in the right hand information box of a request on the Customer Portal.

## Intelligent Capture Settings
`servicemanager.progressiveCapture.servicedetails.enableSupportVisibility`
- The default setting for this is 'Off'
- When the setting is 'On' the Services displayed on the Progressive Capture Service's form will be filtered to both those which the customer is subscribed too, and also to those Services which the analyst's logging the requests team's Support.

`app.request.questions.hideUnansweredQuestions`
- The default setting for this is 'Off'
- When the setting is 'On' any unanswered questions from custom forms used in progressive capture will not be displayed in the Questions section on Request forms

`app.itsm.progressiveCapture.organizationDetails.allowOrgRequestsList`
- The default setting for this is 'Off'
- When the setting is 'On' the analyst viewing the Progressive Capture Organization Details form, will see the active requests for the organization in the righthand panel
- The requests returned will be active, and will only display the requests raised against services which the viewing analyst's teams support.

`app.itsm.progressiveCapture.customerDetails.showOnlySupportedRequests`
- The default setting for this is 'Off'
- This setting determines whether an agent is granted visibility to unsupported customer Requests in the 'Customer Search', 'Contact Search' or 'Co-worker Search' forms in Progressive Capture. When disabled, an agent will have visibility to unsupported customer Requests, this must be avoided for customers with multiple service desks (e.g. IT and HR).

## Request List Settings
`com.hornbill.servicemanager.requestList.restrictions.service`
- The default setting for this is 'ON'
- When this setting is on, it is only possible to perform multi-select actions against requests logged against the same service. If selecting requests logged against different services the multi-select action buttons will be hidden
- When the setting is off, it is possible to perform multi-select actions against requests logged against different services

`com.hornbill.servicemanager.requestList.restrictions.type`
- The default setting for this is 'ON'
- When this setting is on, it is only possible to perform multi-select actions against requests of the same type. If selecting requests of different types, the multi-select action buttons will be hidden
- When the setting is off, it is possible to perform multi-select actions against requests of any types.
Information By turning off the multi-select restrictions, the supporting teams logic is disabled on the assign option on the request list, making it possible to assign requests to teams which are not listed as supporting the services which requests are logged against.

`webapp.view.ITSM.serviceDesk.requests.list.enableNoTeamAllUsers`
- The default setting for this is 'OFF'
- When the setting is on, it is possible for ANY Service Manager subscriber to see any requests which are not assigned to any team
- When the setting is off, it is only possible for Service Manager subscribers with the Service Desk Admin role to see any requests which are not assigned to any teams
Request Settings

`app.request.questions.excludeConditionalQuestions`
- The default setting for this in 'OFF'
- When the setting is off, conditional progressive capture questions which were not displayed in progressive capture flows will appear in the Questions section on the request forms
- When the setting is on, conditional progressive capture questions which were not displayed in progressive capture flows will not appear in the Questions section on the request forms

## Timeline Settings
`guest.servicemanager.request.timeline.showShortPostTitle`
- When this setting is on, it will display the name of the user who posted on the timeline of the request, when viewing the timeline of the request in the Customer and Service Portals.
- When the setting is off, the name of the user who performed the post can still be viewed by hovering over the image of the user on each post.
- The default setting for this is 'ON'

`servicemanager.request.timeline.showShortPostTitle`
- When this setting is on, it will display the name of the user who posted on the timeline of the request in the user app, when viewing the timeline of the request.
- When the setting is off, the name of the user who performed the post can still be viewed by hovering over the image of the user on each post.
- The default setting for this is 'ON'

`guest.servicemanager.request.timeline.availablePostTypes.editPost`
- This setting determines the type of posts that a user is allowed to edit. By selecting additional post types, this will allow a user to edit their own post in a Timeline, provided that the post has not been liked or commented on.
- The default setting for this is 'None' i.e. the option to edit a post will be disabled.
Configuration Management Settings

`app.cm.explorer.diagram.expand`
* These are the entities that can be expanded in the Explorer. The entities with 'false' will have no icon expand/collapse. If a new entity is added in the future in the Conf. Manager app, and this object is not updated with the new entity name, then its value will be set to the default value, which is 'false' (i.e. the user will not be able to expand/collapse the nodes for that entity). The entities currently shown in the diagram are Asset, Colleagues, Contact, Attachment, Requests, Services.
* Default Settings
    "Asset" : true,
    "Colleagues" : false,
    "Contact" : false,
    "Attachment" : false,
    "Requests" : true,
    "Services" : true,
    "default" : false

`app.cm.explorer.diagram.level.max`
* The max level shown in the explorer. Min value is 2 (root plus children)
* Default Setting 3

`app.cm.explorer.items.dependencies`
* This setting holds the possible dependencies that can be set between two entities. 
* The possible entities are Asset, Colleagues, Contact, Attachment, Requests, Services. The property "defs" hold all possible list of values. To associate a list to two linked entities, you must add a property by following this rule: From + entity1 + To + entity2, where entity1 and entity2 can be any value chosen from Asset, Colleagues, Contact, Attachment, Requests, Services. If the two entities are the same (for example 2 assets), then you may define the list of possible values as AssetFromParentToChild and AssetFromChildToParent. For other entities works the same way. Any missing value will detault to the list in defs.default.

"defs" : {
"set1" : ["Connected To", "Depends On", "Installed On"],
"set2" : ["Connected To", "Depends On", "Installed On"],
"default" : ["Connected To", "Depends On", "Installed On"]
         }
"FromAssetToRequests" : "set1",
"FromRequestsToAsset" : "set2",
"FromAssetToServices" : "set2",
"AssetFromParentToChild" : "set2",
"AssetFromChildToParent" : "set2"
app.cm.explorer.items.inPolicy
{{{2}}}
"Asset" : true,
"Colleagues" : true,
"Contact" : true,
"Attachment" : true,
"Requests" : true,
"Services" : true,
"default" : true

<!--https://wiki.hornbill.com/index.php?title=Service_Manager_Settings>