---
layout: article-toc
---
# Roles
Service Manager roles are collections of rights that provide access to the features and functionality within Service Manager. There are system roles and user-defined roles. System roles come with preset rights that are required for users to perform common job roles within the service desk. User-defined roles are for when you need to grant a unique set of rights to a user.

## Topics covered
This article covers the following roles:
* [Asset management](/#asset-management-roles) 
* [Change management](/#change-management-roles) 
* [Incident management](/#incident-management-roles)
* [Knowledge](/#knowledge-roles)
* [Problem management](#problem-management-roles)
* [Release management](#release-management-roles)
* [Service request](#change-management-roles)
* [Services](#services)
* [Administration](#administration-roles)
* [Self Service](#self-service)
* [Reporting](#reporting)
* [Configuration management](#configuration-management-roles)

As well as:
[How to create custom (user-created) roles](#user-created-roles)

## Before you begin
* Have an understanding of how [roles are managed](/esp-config/organizational-data/roles)
::: note
 Assigning a role with a privilege level of `user` or higher to a user can automatically allocate a Service Manager subscription license to that user.
:::

## System roles
System roles are provided when Service Manager is installed or updated. You can assign users to these roles, but the roles cannot be modified.

### Asset management roles
|Role|Description|
|-|-|
|Asset Management Admin|This role is for an Asset Management administrator. It includes rights to define new and edit existing Asset Types, as well as to add detailed Asset information.|
|Asset Management User|This role is for an Asset Management user. It includes rights to define new and edit existing Assets, as well as to add detailed Asset information.|
|Asset Manager|This role should be granted to Asset Managers. It is used for task/activity assignment in the Hornbill Business Process Manager.|
|Software Asset Management User|This role is for a Software Asset Management User. It includes rights to view Software Asset Management records.|

### Change management roles
|Role|Description|
|-|-|
|CAB Approver|This role should be granted to CAB Approvers. It is used for task/activity assignment in the Hornbill Business Process Manager.|
|Change Calendar Viewer|This roles grant read-only access to the Change Calendar and scheduled Change Requests.
|Change Management Full Access|This role is for a senior user of Change Management. It supersedes the Change Management User role and includes rights to cancel and reopen change requests, over-ride locked actions, and complete change activities that are assigned to other users.|
|Change Management User|This role is for a user of Change Management. It includes rights to view, edit, and complete Change Requests.|
|Change Manager|This role should be granted to Change Managers. It is used for task/activity assignment in the Hornbill Business Process Manager.|
|Change Request Assignee|This role should be granted to Users who have the Change Management User role. It is used for task/activity assignment in the Hornbill Business Process Manager.|

### Incident management roles
|Role|Description|
|-|-|
Incident Assignee|This role should be assigned to Users who have the Incident Management User role. It is used for task/activity assignment in the Hornbill Business Process Manager.|
|Incident Management Full Access|This role is for a senior user of Incident Management. It supersedes the Incident Management User role and includes rights to cancel and reopen incident records, over-ride locked actions, and complete incident activities that are assigned to other users.|
|Incident Management User|This role is for users that perform day-to-day work within Incident Management where they are required to raise, manage, and close Incident records.|

### Knowledge roles
|Role|Description|
|:----|:----|
|Knowledge User|This role grants access to browse and view Knowledge content.|
|Knowledge Manager|This role grants access to create and manage knowledge bases. A user must have this role in order to be an owner of a knowledge base. A user with this role can only manage the knowledge bases that they are the owner of.|
|Knowledge Guest Portal|This role grants access to Knowledge content from the Hornbill Customer Portal. It should only be applied to the portal and never granted to any user or guest.|
|Knowledge Contributor|This role grants access to create and update knowledge base articles. Additional access must be granted to perform these functions on private knowledge bases. Knowledge Contributors will become the owner of an article they create and Knowledge Managers can reassign ownership of an article to any user that has both this role and has been granted contributor access to the knowledge base where the article resides.|
|Knowledge Administrator|This role grants access to configuration functionality in Knowledge, including changing ownership of knowledge bases. It should only be assigned to a user on a temporary basis as and when required.|

### Problem management roles
|Role|Description|
|-|-|
|Known Error Assignee|This role should be assigned to Users who have the Problem Management User role. It is used for task/activity assignment in the Hornbill Business Process Manager.|
|Problem Investigation Assignee|This role should be granted to Users who have the Problem Management User role. It is used for task/activity assignment in the Hornbill Business Process Manager.|
|Problem Management Full Access|This role is for a senior user of Problem Management. It supersedes the Problem Management User role and includes rights to cancel and reopen problem records, over-ride locked actions, and complete problem activities that are assigned to other users.|
|Problem Management User|This role is for a user of Problem Management. It includes rights to view, edit, and resolve Problems.|

### Release management roles
|Role|Description|
|-|-|
|Release Assignee|This role should be granted to Users who have the Release Management User role. It is used for task/activity assignment in the Hornbill Business Process Manager.|
|Release Management Full Access|This role is for a senior user of Release Management. It supersedes the Release Management User role and includes rights to cancel and reopen release records, over-ride locked actions, and complete incident activities that are assigned to other users.|
|Release Management User|This role is for a user of Release Management. It includes rights to view, edit, and complete Releases.|
|Release Manager|This role should be granted to Release Managers. It is used for task/activity assignment in the Hornbill Business Process Manager.|

### Service request roles
|Role|Description|
|-|-|
|Service Request Assignee|This role should be granted to Users who have the Service Request User role. It is used for task/activity assignment in the Hornbill Business Process Manager.|
|Service Request Full Access|This role is for a senior user of Service Request Management. It supersedes the Service Request User role and includes rights to cancel and reopen service requests, over-ride locked actions, and complete incident activities that are assigned to other users.|
|Service Request User|This role is for a user of Service Request Management. It includes rights to view, edit, and fulfill Service Requests.|

### Services
|Role|Description|
|-|-|
|Services Manager|This roles provides administrative options to manage services and their content within the Service Portfolio area. A user who is assigned this role can see Services that they own and non-private Services that they support. To see all the Services in the system, you'll need to be in the context of a user who is assigned a role that has "admin" privilege level (e.g. Admin Role or Super User Role).|

### Administration roles
|Role|Description|
|-|-|
|Service Desk Admin|This role is for a Service Desk Administrator. It includes all rights to administrative functions such as setting up support teams as well as being able to cancel requests. Please be aware that assigning this role gives the user the ability to see the details and perform actions on any request on your instance, regardless of their team visibility. This is effectively a Request "Super User" role.|
|Advanced Request Task Completer|This role is for a user who can complete tasks that are assigned to another person. This only applies to requests in Service Manager. Supporting teams of a service that is associated to a request will be respected; otherwise if a request is not associated to a service, then the user can complete tasks that are assigned to the user's team(s) members.|
|All Request Access|This role provides "Super User" functionality as it grants underlying access to all requests, not just those inside an individual user's service subscription model. Note that with this role, a user cannot see requests outside of their service subscription model on the Requests list or when searching for requests through the global search.|
|Service Manager Delete Questions|This role allows Users to delete questions from a Request. It is designed to help remove sensitive information that cannot otherwise be removed or amended.|
|Hornbill Service Manager Integrations|This role is only intended for accounts used to enable integrations or to perform imports.|

### Self service
|Role|Description|
|-|-|
|Self Service User|This role is for a self service User who requires access to the Self Service Portal to be able to raise and view Requests.|
|Self Service Request Cancel|This role is for a self service User who requires access to cancel Service Requests in the Self Service Portal.|
|Service Manager Authorized Guest|This role is for guests accessing the Hornbill Customer Portal.|

### Reporting
|Role|Description|
|-|-|
|Service Manager Reporting|This role grants the user the ability to create, update, and manage all aspects of reporting within Service Manager. This includes measures, widgets, dashboards, slideshows, and reports.|
|Service Manager In-App Reporting|This role provides access to the Reports feature in Service Manager.|


### Configuration management roles
|Role|Description|
|-|-|
|Configuration Manager Admin|This role grants the user the ability to add and modify CI configuration settings such as setting which CIs are in policy and then configuring the two-way relationships between the CI. Assign this role to the main users of the full Configuration Manager app.|
|Configuration Manager User|This role grants a user read-only access to the CI Explorer. This lets the user browse through the linked CIs to help with Incident investigation, problem management, or a view of the impact that something may have. Assign this role to users of Service Manager who need to be able to launch the CI Explorer from a request, asset, or a service, but who do not need full access to the Configuration Manager app.|

## User-created roles
When you need to grant a unique set of rights that is not covered by the system roles, you can create a custom role.

1. Click **+ Create New Role**.
1. Provide a unique ID.  This cannot be the same as any other role.
1. Choose a [privilege level](/esp-config/organizational-data/roles#privileges).
1. Select the [type of role](/esp-config/organizational-data/roles#role-types).
1. Save the role.

### Application rights
A role created under the context of an application will have an `Application Rights` tab where rights that are specific to the app are provided.

#### Service desk
|Right|Description|
|-|-|
|View Service Desk||
|Administer Service Desk||
|View Requests||
|Update Requests|| 
|View Incidents||
|Create Incidents|| 
|Update Incidents||
|Resolve Incidents|| 
|Close Incidents||
|Cancel Incidents||
|Reopen Incidents||
|View Service Requests||
|Create Service Requests|| 
|Update Service Requests||
|Resolve Service Requests|| 
|Close Service Requests|| 
|Cancel Service Requests|| 
|Reopen Service Requests|| 
|View Customer Records|| 
|Export Requests List|| 
|Manage Boards|| 
|View Self Service|| 
|Register Devices|| 
|restartBPMProcess|| 
|Manage Portal Settings|| 
|Update Locked Incidents|| 
|Advanced Request Task Completer|| 
|Update Locked Service Requests||
|Delete Questions||
|View Reports Module|| 
|updateAnswers||
|manageSnippets||
|All Request Access||

#### Problem management
|Right|Description|
|-|-|
|View Problem Management|| 
|Administer Problem Management||
|View Problems||
|Create Problems|| 
|Update Problems||
|Resolve Problems||
|Close Problems||
|Cancel Problems||
|Reopen Problems||
|View Known Errors|| 
|Create Known Errors|| 
|Update Known Errors||
|Resolve Known Errors||
|Close Known Errors|| 
|Cancel Known Errors|| 
|Update Locked Problems|| 
|Update Locked Known Errors|| 
|Reopen Known Errors|| 

#### Change and release Management
|Right|Description|
|-|-|
|View Change Management|| 
|Administer Change Management||
|View Changes||
|Create Changes|| 
|Update Changes||
|Resolve Changes||
|Close Changes||
|Cancel Changes||
|reopenChangeRequests||
|View Release Management|| 
|administerReleaseManagement||
|View Releases||
|Create Releases|| 
|Update Releases|| 
|Close Releases|| 
|Cancel Releases|| 
|Reopen Releases|| 
|Resolve Releases|| 
|Update Locked Change Requests||
|Update Locked Releases|| 
|restrictChangeCalendar||

#### Asset management
|Right|Description|
|-|-|
|View Asset Management|| 
|View Asset Audit Trail||
|Administer Asset Management||
|View CMS||
|View Configuration Items||
|Create Configuration Items|| 
|Edit Configuration Items||
|Delete Configuration Items|| 
|viewSoftwareInventory||
|View Configuration Management||

#### Service level management
|Right|Description|
|-|-|
|View Service Level Management|| 
|View Service Level Requirements|| 
|Create Service Level Requirements|| 
|Edit Service Level Requirements|| 
|Delete Service Level Requirements|| 
|View Service Level Agreements|| 
|Create Service Level Agreements|| 
|Edit Service level Agreements|| 
|Delete Service Level Agreements|| 
|View Service Level Reports|| 
|Create Service Level Reports|| 
|Edit Service Level Reports|| 
|Delete Service Level Reports|| 
|updateRequestServiceLevel||

#### Service management
|Right|Description|
|-|-|
|View Service Records|| 
|Create Service Records|| 
|Edit Service Records|| 
|Delete Service Records|| 
|Manage Subscriptions|| 
|Manage Service Owners|| 

#### Self service
|Right|Description|
|-|-|
|viewIncidents|| 
|viewServiceRequests||
|viewChangeRequests||
|createIncidents||
|createServiceRequests||
|createChangeRequests||
|updateIncidents||
|updateServiceRequests||
|updateChangeRequests||
|closeIncidents||
|closeServiceRequests||
|closeChangeRequests||
|cancelServiceRequests|| 
|reopenIncidents|| 
|reopenServiceRequests||
|reopenChangeRequests||

#### Entities access control
|Right|Description|
|-|-|
|Allow execution of application queries|| 
|Add an Entity Record|| 
|View an Entity Record|| 
|Update an Entity Record|| 
|Delete an Entity Record|| 
|Search Entity Records|| 
|Send Notifications|| 
|executeSystemAPIs|| 
|manageKnowledgeManagement|| 
|viewKnowledgebase||
|manageKnowledgebases|| 
|createKnowledgebases|| 
|editKnowledgebases|| 
|deleteKnowledgebases|| 
|createKnowledgebaseArticle|| 
|editKnowledgebaseArticle|| 
|deleteKnowledgebaseArticle||


<!-- https://wiki.hornbill.com/index.php?title=Service_Manager_Roles -->

<!--

 Knowledge Manager	Security	This role allows users to access knowledge management configuration, and modify knowledge bases, topics, and articles	User

 My Boards	Security	This role is for the now deprecated MyBoards feature within the Service Manager Application.

 SM Knowledge Manager	Security	This role allows Users to administer the Knowledge, modifying knowledge bases and articles.
 -->
