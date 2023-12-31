---
layout: article-toc
---
# Roles
Service Manager roles are collections of rights that provide access to different features and functionality within Service Manager. System roles are provided with preset rights that are required for users to perform common job roles within the Service Desk.  User defined roles can also be created.

## Topics Covered
* Asset Management Roles
* Change Management Roles
* Incident Management Roles
* Problem Management Roles
* Release Management Roles
* Service Request Roles
* System and Application Roles
* Configuration Management Roles

## Before you Begin
* Have an understanding of how [roles are managed](/esp-config/organizational-data/roles)
::: tip
 Assigning a role with a privilege level of `user` or higher to a user can automatically allocate a Service Manager subscription license to that user.
:::

## System Roles
System roles are provided when Service Manager is installed or updated.  These roles can not be modified, other than assigning users to the roles.

### Asset Management Roles
|Role|Description|
|-|-|
|Asset Management Admin|This role is for an Asset Management administrator. It includes rights to define new and edit existing Asset Types as well as being able to add detailed Asset information|
|Asset Management User|This role is for an Asset Management user. It includes rights to define new and edit existing Assets as well as being able to add detailed Asset information.|
|Asset Manager|This role should be granted to Asset Managers. It is used for task/activity assignment in the Hornbill Business Process Manager.|
|Software Asset Management User|This role is for a Software Asset Management User. It includes rights to view Software Asset Management records.|

### Change Management Roles
|Role|Description|
|-|-|
|CAB Approver|This role should be granted to CAB Approvers. It is used for task/activity assignment in the Hornbill Business Process Manager.|
|Change Calendar Viewer|This roles grant read only access to the Change Calendar and scheduled Change Requests.
|Change Management Full Access|This role is for a senior user of Change Management. It supersedes the Change Management User role and includes rights to cancel and reopen Change Requests.|
|Change Management User|This role is for a user of Change Management. It includes rights to view, edit and complete Change Requests.|
|Change Manager|This role should be granted to Change Managers. It is used for task/activity assignment in the Hornbill Business Process Manager.|
|Change Request Assignee|This role should be granted to Users who have the 'Change Management User' role. It is used for task/activity assignment in the Hornbill Business Process Manager.|

### Incident Management Roles
|Role|Description|
|-|-|
Incident Assignee|This role should be assigned to Users who have the 'Incident Management User' role. It is used for task/activity assignment in the Hornbill Business Process Manager.|
|Incident Management Full Access|This role is for a senior user of Incident Management. It supersedes the Incident Management User role and includes rights to cancel and reopen Incidents.|
|Incident Management User|This role is for a users that perform day to day work within Incident Management where they are required to raise, manage, and close Incident records.|

### Problem Management Roles
|Role|Description|
|-|-|
|Known Error Assignee|This role should be assigned to Users who have the 'Problem Management User' role. It is used for task/activity assignment in the Hornbill Business Process Manager.|
|Problem Investigation Assignee|This role should be granted to Users who have the 'Problem Management User' role. It is used for task/activity assignment in the Hornbill Business Process Manager.|
|Problem Management Full Access|This role is for a senior user of Problem Management. It supersedes the Problem Management User role and includes rights to cancel and reopen Problems.|
|Problem Management User|This role is for a user of Problem Management. It includes rights to view, edit and resolve Problems.|

### Release Management Roles
|Role|Description|
|-|-|
|Release Assignee|This role should be granted to Users who have the 'Release Management User' role. It is used for task/activity assignment in the Hornbill Business Process Manager|
|Release Management Full Access|This role is for a senior user of Release Management. It supersedes the Release Management User role and includes rights to cancel and reopen Release
|Release Management User|This role is for a user of Release Management. It includes rights to view, edit and complete Releases|
|Release Manager|This role should be granted to Release Managers. It is used for task/activity assignment in the Hornbill Business Process Manager|

### Service Request Roles
|Role|Description|
|-|-|
|Service Request Assignee|This role should be granted to Users who have the 'Service Request User' role. It is used for task/activity assignment in the Hornbill Business Process Manager.|
|Service Request Full Access|This role is for a senior user of Service Request Management. It supersedes the Service Request User role and includes rights to cancel and reopen Service Requests.|
|Service Request User|This role is for a user of Service Request Management. It includes rights to view, edit and fulfill Service Requests.|

### Services
|Role|Description|
|-|-|
|Services Manager|This roles provides administrative options to manage services and their content within Service Portfolio area. A user who is assigned this role will be able to see Services that they own and non-private Services that they support. To see all the Services in the system, you'll need to be in context of a user who is assigned a role that has "admin" privilege level (E.g. Admin Role or Super User Role).|

### Administration Roles
|Role|Description|
|-|-|
|Service Desk Admin|This role is for a Service Desk Administrator. It includes all rights to administrative functions such as setting up support teams as well as being able to cancel requests. Please be aware that assigning this role gives the user the ability to see the details and perform actions on any request on your instance, regardless of their team visibility. This is effectively a Request "Super User" role.|
|Advanced Request Task Completer|This role is for a user who can complete tasks that are assigned to another person. This only applies to requests in Service Manager. Supporting teams of a service that is associated to a request will be respected otherwise if a request is not associated to a service, then the user can complete tasks that are assigned to the user's team(s) members.|
|All Request Access|This role provides super user functionality as it grants underlying access to all requests, not just those inside an individual user's service subscription model. Note, with this role a user will not see requests outside of their service subscription model on the request list or when searching for requests through the global search.|
|Service Manager Delete Questions|This role allows Users to delete questions from a Request, designed to help remove sensitive information that cannot otherwise be removed or amended.|
|Hornbill Service Manager Integrations|This role is only intended for accounts used to enable integrations or to perform imports.|

### Self Service
|Role|Description|
|-|-|
|Self Service User|This role is for a self service User that requires access to Self Service Portal to be able to raise and view Requests.|
|Self Service Request Cancel|This role is for a SelfService User that requires access to Cancel Service Requests in the SelfService Portal|
|Service Manager Authorized Guest|This role is for guests accessing the Hornbill Customer Portal.|

### Reporting
|Role|Description|
|-|-|
|Service Manager Reporting|This Role grants the user the ability to create, update, and manage all aspects of reporting within Service Manager. This includes measures, widgets, dashboards, slideshows, and reports|
|Service Manager In-App Reporting|This role provides access to the Reports feature in Service Manager.|


### Configuration Management Roles
|Role|Description|
|-|-|
|Configuration Manager Admin|This role gives someone the ability to add and modify CI configuration settings such as setting which CIs are in policy and the configuring the two way relationships between the CI. Assign this role to the main users of the full Configuration Manager app.|
|Configuration Manager User|This role is great for giving a user read-only access to the CI explorer. This lets them browse through the linked CIs to help with Incident investigation, problem management, or a view of the impact that something may have. Assign this role to user of Service Manager that need to be able to launch the CI Explorer from a request, asset, or a service, but do not need full access to the Configuration Manager app.|

## User Created Roles
When a unique set of right is required that is not covered by the system roles, a custom role can be created.

1. Click on `+ Create New Role`
1. Provide a unique ID.  This can not be the same as any other role.
1. Choose a [privilege level](/esp-config/organizational-data/roles#privileges).
1. Select the [type of role](/esp-config/organizational-data/roles#role-types).
1. Save the role.

### Application Rights
A role created under the context of an application will have a `Application Rights` tab where rights that are specific to the app are provided.

#### Service Desk
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

#### Problem Management
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

#### Change and Release Management
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

#### Asset Management
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

#### Service Level Management
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

#### Service Management
|Right|Description|
|-|-|
|View Service Records|| 
|Create Service Records|| 
|Edit Service Records|| 
|Delete Service Records|| 
|Manage Subscriptions|| 
|Manage Service Owners|| 

#### Self Service
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

#### Entities Access Control
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
