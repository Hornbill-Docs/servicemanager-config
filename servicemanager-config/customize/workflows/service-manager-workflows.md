---
layout: article-toc
---
# General Request Automation
The Service Manager Workflows are used to automate the processing of the requests that have been raised. This page contains information on the Service Manager automated tasks that can be used in the Workflow Designer to build unique and powerful workflows for your requests.


### Access Control
Use the Access Control to lock or unlock the Details section or the Actions on a request. Only users with the appropriate application right (update locked requests) will be able to modify the details or use an Action once locked. This right has been added to the following roles: Incident Management Full Access, Change Management Full Access, Problem Management Full Access, Release Management Full Access, Service Request Full Access, and Service Desk Admin.

* Lock / Unlock Request Actions
* Lock Request Details
* Unlock Request Details

### Assessment
Use the Assessment node to initiate an Impact Assessment on a request.

This Hornbill Automation will present an Impact Assessment option on the Escalate Action of a request. When selected, a user is taken through a number of defined questions; based on the user's responses, an impact level is automatically applied to the request.

### Assets
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

### Assignment
Use the Assignment node to automatically assign a request to different Service Manager users or teams.

* **Assign to Service Team**<br>Use this option to assign the request to the team that supports the service. If no team supports the service that the request is logged against, then the request is not assigned. If more than one team supports the service, the request is assigned to the team that has supported the service the longest. This automated task does not assign the request to an individual within the team(s) supported by the service.
* **Assign to Team**<br>Use this option to assign the request to a specified team.
* **Assign to Owner**<br>Use this option to assign the request to a specific Service Manager agent.
* **Assign to Owner (Variable)**<br>Use this option to assign the request to a specific Service Manager analyst using a dynamic value provided by a runtime variable that has been populated using Intelligent Capture or through the Get Information nodes.
* **Unassign Owner**<br>Use this option to remove the current owner from the request without affecting the team to which the request is assigned.  
* **Assign to Request Creator**<br>Use this option to automatically assign the request to the Service Manager agent who raised the request.
* **Assign to Most Available Analyst**<br>This automation works on the basis of capacity. The system will look through the members of the selected team and will assign the request to the member who has the least amount of open requests. If multiple team members have an equal number of open requests and have the least amount of assigned requests, the system will allocate the request to the team member who has had the greatest amount of time pass since their last assignment.
* **Assign on Round Robin Basis**<br>Round robin assignment is a great way to automatically assign requests to the members of a team. The system will look through the members of the selected team and will assign the request to the member who has had the greatest amount of time pass since their last assignment. The system will take into account the user's status, which is found on their profile. If the user's status is set to anything other than *Available*, that user will not be considered for assignment. This does not take into account the volume of requests assigned to each user.

### Authorization Decision
Use the Authorization Decision node to mark on a Change or Service Request form if an authorization decision has been made.

* Approved
* Rejected
* Clear

### Collaboration
Use the Collaboration node to post an automated update onto a public workspace at any stage in a workflow. This will be visible to members of the specified workspace --- on the timeline of the workspace and in members' News Feeds.

* Comment on Existing Public Workspace Post
* Comment on Request Source Post
* Post to Public Workspace

### Email Notifications
Use the Email Notification nodes to send email templates to different Request stakeholders. Configuration options include recipient, which email template to use, and which mailbox to send the email from.

* Email Contact
* Email Co-worker
* Email Customer
* Email Customer Manager
* Email External Address
* Email Request Owner

### Get Request Information
Use the Get Request Information node at any stage in a workflow and preceding another workflow node when you want to make the variables of the Request available. Variables may include Customer, Status, Site, Priority, or any Answers to Customer defined questions from different Progressive capture forms or attributes of the customer or organization of the request the workflow is running against.

* **Category Details**<br>This is designed to get information about both the request category and the resolution category. Ideal for making decisions based on the selected category.
* **Customer Details**<br>Get more information about the customer to help drive the workflow.  Find out who their manager is. Check the custom fields for things like VIP status.
* **Source Email Details**<br>If the request was raised from an email, you can use this to get details such as the email of the sender.  This is particularly useful when the contact or user does not exist in your system.
* **Organization Details**<br>Use when supporting external organizations.  This can be particularly useful to check for information stored in the custom fields of the organization.  Find out the location of the organization to determine which service desk or team to assign the request to.
* **Owner Details**<br>Can be used if you need more detail about the request owner than what the Request Details provide. A commonly used output is the owner's manager.
* **Raised By Details**<br>Gather information about who raised the request.  This can be particularly useful on request types that don't include customers.  For example, you may want to include some automation on a change workflow that communicates back to the person who raised the change.
* **Request Details**<br>This returns all the key information about a request.  Possibly one of the most used automations in a request workflow. 
* **Progressive Capture Answers**<br>This lets you interrogate the answers that were provided during the capture phase of a request.  Make decisions based on the provided answers to drive your workflow.   
* **Service Details**<br>Get the details of the associated service. When a request is first raised you may want to check the status of the service and send an automated email to the customer about the service not being available.  
* **Site Details**<br>Your workflow may have location specific responses to an issue.  Use the Manager IDs to help communicate issues at a site.  You could add the managers as a connection or send them a notification of high priority incidents.
* **Team Details**<br>Get information about the team that the request is currently assigned to.  Two useful outputs are the IDos of the team's manager and leader, allowing you to send notifications, escalate, or add as a member.

### Integration
Use the Integration node at any stage of a workflow, where you wish to invoke specific actions against a 3rd party application from the available list of applications.

* Create Jira Request
* Add Jira Request Comment
* Log New Service Request

### Linked Requests
Use the Linked Requests node to automatically post updates and resolve linked Requests. Linked requests are those that have been linked using the Link Action Item on a request form.

* Resolve Linked Requests
* Update Linked Requests

### Log Requests
Use the Log Request to automatically raise another request at a particular point in the workflow.

* Log New Change
* Log New Incident
* Log New Known Error
* Log New Problem
* Log New Release
* Log New Request

:::note
Using these options in your workflows, please be aware of where you are invoking them / placing them in the workflow, and in turn which workflows are going to be invoked against the new Incident or Service Request raised. Please avoid scenario's where one workflow may invoke the logging of a new request, where the new request's workflow immediately is configured to log a new request which again has a workflow which again logs another request immediately creating a loop. The result of which may be a lot of unwanted requests. In the event this occurs, disable the causing workflow and resolve the issue.
:::

### Questions
* Delete Questions

### Request Service
The Request Service Tasks are used to automate the linking of related services that may underpin or depend on the service that the request is raised under.  This is equivalent to the [Linked Services Action](/servicemanager-user-guide/service-portfolio/requests/linked-services-action) on a request where services can be manually linked. 

* **Add Related Services**<br>A business service can be underpinned by technical services or an issue with a technical service may impact the services that depend on it.  This task will look at the service under which the request was raised and then link all of the related services based on a particular type of relationship. 
* **Add Linked Service**<br>This task allows for a single service to be added to the list of associated services to the request.  Rather than associating all services based on relationship type, this allows for a single service to be linked.
* **Update Service Status**<br>This task allows for the [Service Status](/servicemanager-user-guide/service-portfolio/services/service-availability) to be updated on all of the linked services to help determine the availability of those services.  

### Suspend
Use the Suspend nodes if you wish to suspend the progress of the workflow until a defined action is performed manually on the Request. This could include waiting for a Priority to be set, a Customer added, Ownership set or the Resolution defined. Configuration options include the ability to specify the context (which Action Bar icon) the Request will appear in whilst waiting for the Suspend (manual action) to be performed.

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

### Update Request
Use the Update Request node to automatically update the values of specific Request attributes at any stage in the workflow. Examples being updating the Logging or Closing Categories of a Request.

* Logging Category
* Closure Category
* Update Customer
* Update Custom Fields
* Details
* External Reference
* First Time Fix
* Place On Hold
* Priority
* Resolution Text
* Service
* Service Level
* Site
* Site (Customer' Site)
* Source
* Status / Sub-status
* Timeline

### Request Timers
Use the Request Timer nodes at any stage in the workflow to either start or stop the Response and or Resolution timers. It is not a perquisite to have to use any timers within workflows or to have to use both Response and Resolution timers when timers are used.

There are some settings that control the default behavior of the Service Level Timers. The settings provided to pause or stop the resolution timer when resolving a request are as follows:

app.request.pauseResolutionTimerOnResolve (Default OFF)
app.request.resumeResolutionTimerOnReopen (Default OFF)
app.request.stopResolutionTimerOnResolve (Default ON)
app.request.stopResolutionTimerOnClose (Default OFF)

Using settings to control resolution timers
You should choose the relevant settings to meet your needs, but note that app.request.stopResolutionTimerOnResolve will take precedence over app.request.pauseResolutionTimerOnResolve so ensure only the one you want to use is enabled.
Using BPM nodes to control resolution timers
If you are using this BPM node to control resolution timers the four settings above should all be turned off; If any settings are enabled then they will take precedence over BPM actions. To enable pause/resume of a resolved request you can add the Timer > Pause Resolution Timer or Timer > Resume Resolution Timer BPM nodes as required in your workflow.

* Start Resolver Timer
* Stop Resolution Timer
* Start Response Timer
* Stop Response Timer
* Pause Resolution Timer
* Resume Resolution Timer

<!-- https://wiki.hornbill.com/index.php?title=Service_Manager_Business_Process_Workflow -->