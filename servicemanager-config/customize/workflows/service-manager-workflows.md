---
layout: article-toc
---
# Request Automation
The Service Manager Workflows are used to automate the processing of the requests that have been raised. This page contains information on the Request Automation that can be used in the Workflow Designer to build unique and powerful workflows for your requests.

## Access Control
Use the Access Control to lock or unlock the details section or the Actions on a request. Only users with an appropriate role or application right will be able to use a locked action or have the ability to unlock the action for others to use.

![Workflow Lock Automation](/_books/servicemanager-config/images/workflow-lock-automation.png)

### Example uses
* On an incident, the resolution action could be locked until other actions have been completed.
* On a change, the details might be locked once a change has been approved.
* Only allow full access users the ability to apply certain actions. 

![Worflow Lock Action](/_books/servicemanager-config/images/workflow-lock-action.png)

### Available tasks
* **Lock / Unlock Request Actions**. Lock or unlock individual actions on a request.  The option *Default Lock Type* can apply or remove the locks from all actions.
* **Lock Request Details**.  Lock the main details section of the request. This includes both the summary and description.
* **Unlock Request Details**. Unlock the main details section of the request. This includes both the summary and description.

### Overriding a locked action
Users that have a [Full Access](/servicemanager-config/setup/service-manager-roles#system-roles) role can override a locked action for the request type that they have full access to.  They can themselves use the locked action, or they can click on the padlock icon to unlock the action for other users.

![Locked Resolution Action](/_books/servicemanager-config/images/request-locked-resolution.png)

:::tip
An **Update Locked** application right is available for each request type.  [Custom roles](/esp-config/organizational-data/roles#user-created-roles) can be created with these rights to provide access to select users without having to give them full access to a request type. 
:::

## Assessment
Use the Assessment automation to initiate an Assessment Questionnaire on a request.

This Hornbill Automation will present an [Assessment Questionnaire](/servicemanager-config/administration/assessment-questionnaires) on the [Assessment Action](/servicemanager-user-guide/service-portfolio/requests/assessment-action) of a request. Based on the user's responses to the questionnaire, an assessment level is automatically calculated and applied to the request.

### How to add a Log Request automation
1. Add a Hornbill Automation node to the workflow.
1. Open the node’s settings by clicking on the cog icon.
1. Under the Scope field select Entity.
1. Under the Entity field select Requests.
1. Under the Type field select Assessment.
1. Under the Task field select the type of assessment.

![Assessment Automation](/_books/servicemanager-config/images/workflow-assessment.png)

### Available tasks
* Impact
* Priority
* Risk
* Urgency

### Options
#### Mandatory Options
* **Request ID**. In almost all cases this should be set to Auto. The Request ID is a predefined input parameter that contains the Request ID of the request that the workflow is associated with.
* **Assessment**. This option will need to be set to **Manual** and then one of the available assessment questionnaires needs to be selected.

## Assets
Use these Hornbill Automations for managing assets that are associated to the request:
* Add All Owned by Customer
* Add Generic Assets Owned by Customer
* Add Computer System Assets Owned by Customer
* Add Computer Peripheral Assets Owned by Customer
* Add Mobile Device Assets Owned by Customer
* Add Network Device Assets Owned by Customer
* Add Printer Assets Owned by Customer
* Add Software Assets Owned by Customer
* Add Telecoms Assets Owned by Customer
* Create Generic Asset
* Create Computer System Asset
* Create Computer Peripheral Asset
* Create Mobile Device Asset
* Create Network Device Asset
* Create Printer Asset
* Get All Assets
* Get All Generic Assets
* Get All Computer Peripheral Assets
* Get All Mobile Device Assets
* Get All Network Device Assets
* Get All Printer Assets
* Get All Software Assets
* Get All Telecoms Assets
* Update All Assets - General Information
* Update Computer Assets - Additional Properties
* Update Computer Assets - General Information
* Update Computer Peripheral Assets - Additional Properties
* Update Computer Peripheral Assets - General Information
* Update Mobile Device Assets - Additional Properties
* Update Mobile Device Assets - General Information
* Update Network Device Assets - Additional Properties
* Update Network Device Assets - General Information
* Update Printer Assets - Additional Properties
* Update Printer Assets - General Information
* Update Software Assets - Additional Properties
* Update Software Assets - General Information
* Update Telecoms Assets - General Information

## Assignment
Use the Assignment node to automatically assign a request to different Service Manager users or teams.

* **Assign to Service Team**<br>Use this option to assign the request to the team that supports the service. If no team supports the service that the request is logged against, then the request is not assigned. If more than one team supports the service, the request is assigned to the team that has supported the service the longest. This automated task does not assign the request to an individual within the team(s) supported by the service.
* **Assign to Team**<br>Use this option to assign the request to a specified team.
* **Assign to Owner**<br>Use this option to assign the request to a specific Service Manager agent.
* **Assign to Owner (Variable)**<br>Use this option to assign the request to a specific Service Manager analyst using a dynamic value provided by a runtime variable that has been populated using Intelligent Capture or through the Get Information nodes.
* **Unassign Owner**<br>Use this option to remove the current owner from the request without affecting the team to which the request is assigned.  
* **Assign to Request Creator**<br>Use this option to automatically assign the request to the Service Manager agent who raised the request.
* **Assign to Most Available Analyst**<br>This automation works on the basis of capacity. The system will look through the members of the selected team and will assign the request to the member who has the least amount of open requests. If multiple team members have an equal number of open requests and have the least amount of assigned requests, the system will allocate the request to the team member who has had the greatest amount of time pass since their last assignment.
* **Assign on Round Robin Basis**<br>Round robin assignment is a great way to automatically assign requests to the members of a team. The system will look through the members of the selected team and will assign the request to the member who has had the greatest amount of time pass since their last assignment. The system will take into account the user's status, which is found on their profile. If the user's status is set to anything other than *Available*, that user will not be considered for assignment. This does not take into account the volume of requests assigned to each user.

## Authorization Decision
Use the Authorization Decision node to mark a Change or Service Request with the current status of an authorization. This works independently of any particular type of authorization. Setting the authorization decision will typically follow the outcome of an authorization however it can also be used in any circumstance where some form of acceptance to proceed is required.

![Authorization Decision Automation](/_books/servicemanager-config/images/workflow-authorization-decision.png)

### Available Tasks
* Approved
* Clear
* Pending
* Rejected

### Using the Authorization Decision
Each time the Authorization Decision is used in the workflow, the request is updated with this decision.  This can be seen within the request's information panel.

![Authorization Decision on a request](/_books/servicemanager-config/images/request-authorization-decision.png)

The Advanced Filter and [Views](/servicemanager-user-guide/request-list/views) on the request list can also be used to display requests based on their different authorization states.

### Workflow Example
This is an example of how the Authorization Decision could be used when designing a workflow.
* Prior to an authorizaton, the Authorization Decision can be set to **Pending**.
* Once an authorization has taken place, a decision node can be used to branch the workflow based on the outcome of the authorization.
* If rejected, the authorization decision is set to **Rejected**.
* If approved, the authorization decision is set to **Approved**.
* If no match, which might be the result of the authorization expiring, the original **Pending** can be cleared before continuing with the workflow.

![Authorization Decision Example](/_books/servicemanager-config/images/workflow-authorization-decision-example.png)

## Collaboration
Use the Collaboration node to post an automated update onto a public workspace at any stage in a workflow. This will be visible to members of the specified workspace --- on the timeline of the workspace and in members' News Feeds.

* Comment on Existing Public Workspace Post
* Comment on Request Source Post
* Post to Public Workspace

## Email Notifications
Use the Email Notification nodes to send email templates to different Request stakeholders. Configuration options include recipient, which email template to use, and which mailbox to send the email from.

* Email Contact
* Email Co-worker
* Email Customer
* Email Customer Manager
* Email External Address
* Email Request Owner

## Get Request Information
Use the Get Request Information node at any stage in a workflow and preceding another workflow node when you want to make the variables of the Request available. Variables may include Customer, Status, Site, Priority, or any answers to customer-defined questions from different Intelligent Capture forms or attributes of the customer or organization of the request the workflow is running against.

* **Category Details**<br>This is designed to get information about both the request category and the resolution category. Use this for making decisions based on the selected category.
* **Customer Details**<br>Get more information about the customer to help drive the workflow.  Find out who their manager is. Check the custom fields for things like VIP status.
* **Source Email Details**<br>If the request was raised from an email, you can use this to get details such as the email of the sender.  This is particularly useful when the contact or user does not exist in your system.
* **Organization Details**<br>Use when supporting external organizations.  This can be particularly useful to check for information stored in the custom fields of the organization.  Find out the location of the organization to determine which service desk or team to assign the request to.
* **Owner Details**<br>Use this if you need more detail about the request owner than what the Request Details provide. A commonly used output is the owner's manager.
* **Raised By Details**<br>Gather information about who raised the request.  This can be particularly useful on request types that don't include customers.  For example, you may want to include some automation on a change workflow that communicates back to the person who raised the change.
* **Request Details**<br>This returns all the key information about a request.  This is one of the most-used automations in a request workflow. 
* **Intelligent Capture Answers**<br>This lets you interrogate the answers that were provided during the capture phase of a request.  Make decisions based on the provided answers to drive your workflow.   
* **Service Details**<br>Get the details of the associated service. When a request is first raised, you may want to check the status of the service and send an automated email to the customer about the service not being available.  
* **Site Details**<br>Your workflow may have location-specific responses to an issue.  Use the Manager IDs to help communicate issues at a site.  You could add the managers as a connection or send them a notification of high-priority incidents.
* **Team Details**<br>Get information about the team that the request is currently assigned to.  Two useful outputs are the IDs of the team's manager and leader, allowing you to send notifications, escalate, or add as a member.

## Integration
Use the Integration node at any stage of a workflow, where you wish to invoke specific actions against a third-party application from the available list of applications.

* Create Jira Request
* Add Jira Request Comment
* Log New Service Request

## Linked Requests
Use the Linked Requests node to automatically post updates and resolve linked requests. Linked requests are those that have been linked using the Link Action Item on a request form.

* Resolve Linked Requests
* Update Linked Requests

## Log Request
Use the Log Request node to automatically log another request at a particular point in the workflow. This can be used when an additional request is required to fulfill the original request.  For example, an incident might result in the raising of a problem or change request. Another example might be a service request for initiating a new starter.  Additional requests can be raised for different teams or areas within the business to fulfill. 

When a new request is logged, it will be automatically linked to the request from which it was raised.

### Before you begin
* Make sure that the request type being logged is enabled in the service that the request is being logged under.
* Make sure that service subscriptions are in place for new requests that require a customer. 
* Be familiar with the workflow that will be used in the new request and the data that is required to fulfill the workflow.
* Be aware of loops.  Avoid situations in the workflow where the logging of one request leads to the logging of another, and potentially ending up in a loop.

### How to add a Log Request automation
1. Add a Hornbill Automation node to the workflow.
1. Open the node’s settings by clicking on the cog icon.
1. Under the Scope field select Entity.
1. Under the Entity field select Requests.
1. Under the Type field select Log Request.
1. Under the Task field select the type of request to be logged.

![Log New Automation](/_books/servicemanager-config/images/workflow-log-new.png)

### Available tasks
* Log New Change
* Log New Incident
* Log New Known Error
* Log New Problem
* Log New Release
* Log New Request

### Options
The **Options** allow you to pre-populate the new request with information. The options that start with "Copy" will take the values directly from the request that it is being logged from. 

#### Mandatory Options
* **Request ID**. In almost all cases this should be set to Auto. The Request ID is a predefined input parameter that contains the Request ID of the request that the workflow is associated with.

:::important
Make sure that the new request being logged has all the information required to fulfill the workflow it is using. 
:::

### Output
The output of this Hornbill Automation is the ID of the new request.  This can be used within the same workflow to make additional updates to the new request after it has been logged.

## Questions
* Delete Questions

## Request Service
The Request Service Tasks are used to automate the linking of related services that may underpin or depend on the service that the request is raised under.  This is equivalent to the [Linked Services Action](/servicemanager-user-guide/service-portfolio/requests/linked-services-action) on a request where services can be manually linked. 

* **Add Related Services**<br>A business service can be underpinned by technical services, or an issue with a technical service may impact the services that depend on it.  This task looks at the service under which the request was raised and then links all of the related services based on a particular type of relationship. 
* **Add Linked Service**<br>This task allows for a single service to be added to the list of associated services to the request.  Rather than associating all services based on relationship type, this allows for a single service to be linked.
* **Update Service Status**<br>This task allows for the [Service Status](/servicemanager-user-guide/service-portfolio/services/service-availability) to be updated on all of the linked services to help determine the availability of those services.  

## Suspend
Use a Suspend node if you wish to suspend the progress of the workflow until a defined action is performed manually on the request. This could include waiting for a priority to be set, a customer added, ownership set, or the resolution defined. Configuration options include the ability to specify the context (which Action Bar icon) the request will appear in while waiting for the Suspend (manual action) to be performed.

* Await Expiry
* Wait for List of Request Authorizers
* Wait for Attachment
* Wait for Request Closure
* Wait for Request Closure Category
* Wait for Request Connection
* Wait for Custom Field
* Wait for Customer
* Wait for Feedback
* Wait for Request Description
* Wait for Document
* Wait for Request Email
* Wait for External Reference
* Wait for Impact Assessment
* Wait for Linked Assets
* Wait for Linked Request
* Wait for Linked Requests Completion
* Wait for Linked Request Update
* Wait for Linked Services
* Wait for New Request Owner
* Wait for Request Off Hold
* Wait for Request Owner
* Wait for Request Priority
* Wait for Request Category
* Wait for Request Resolution
* Wait for Request Site
* Wait for Status Change
* Wait for Request Summary
* Wait for Request Team
* Wait for Request Update
* Wait for Urgency Assessment

## Update Request
Use the Update Request node to automatically update the values of specific request attributes at any stage in the workflow. 

### How to add a request update
1. Add a Hornbill Automation node to the workflow.
1. Open the node’s settings by clicking on the cog icon.
1. Under the `Scope` field select `Entity`.
1. Under the `Type` field select `Update Request`.
1. Under the `Task` field select an update task.

![Update Request](/_books/servicemanager-config/customize/workflows/images/update-request.png)

### Common options for tasks
Some options are common to all of the Update Request types.  
* **Request ID**. In almost all cases this should be set to `Auto`. The Request ID is a predefined input parameter that contains the Request ID of the request that the workflow is associated with.

### Available tasks
* **Logging Category**.
* **Closure Category**.
* **Update Customer**.
* **Update Custom Fields**.
* **Details**.
* **External Reference**.
* **First Time Fix**.
* **Place On Hold**.
* **Impact**. This automation for updating the impact of a request uses the impact levels that are defined under the [Impact Assessments](/servicemanager-config/administration/assessment-levels#impact).  Within the Options section of the automation settings, Impact is a mandatory field.  This needs to be set to `Manual` and then an appropriate impact selected.
* **Priority**. This automation for updating the priority of a request uses the priority levels that are defined under the [Priority Assessments](/servicemanager-config/administration/assessment-levels#priority).  Within the Options section of the automation settings, Priority is a mandatory field.  This needs to be set to `Manual` and then an appropriate priority selected.
* **Resolution Text**.
* **Risk**. This automation for updating the risk of a request uses the risk levels that are defined under the [Risk Assessments](/servicemanager-config/administration/assessment-levels#risk).  Within the Options section of the automation settings, Risk is a mandatory field.  This needs to be set to `Manual` and then an appropriate risk selected.
* **Service**.
* **Service Level**.
* **Site**.
* **Site (Customer's Site)**.
* **Source**.
* **Status**.
* **Timeline**.
* **Urgency**. This workflow automation is used for updating the urgency of a request, using the urgency levels that are defined under the [Urgency Assessments](/servicemanager-config/administration/assessment-levels#urgency).  Within the **Options** section of the automation settings, **Urgency** is a mandatory field.  This needs to be set to `Manual` and then an appropriate urgency level selected.

    ![Update Urgency](/_books/servicemanager-config/customize/workflows/images/update-request-urgency.png)

    * When using this workflow automation, you can assess information stored in a request and automatically set the urgency level accordingly.
    * When using this workflow automation, the urgency can be set without having to enable it in the assessment action or create an assessment questionnaire.
    * When the urgency can only be set using workflow automation, it prevents users from manually changing it using the [Assessment Action](/servicemanager-user-guide/service-portfolio/requests/assessment-action#urgency) on a request.