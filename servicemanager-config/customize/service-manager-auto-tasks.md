---
layout: article-toc
---
# Auto Tasks
Auto Tasks provide the ability to execute automation from Custom Buttons on different entity views in apps on the Hornbill platform. Auto tasks are similar to workflows, however differ in that they do not contain stages, don't use tasks or approvals, and can't be suspended. When executed, the Auto Task will simply start > Execute > End. An Auto Task can contain many nodes and therefore execute multiple actions triggered from a single custom button. Auto Tasks can be configured using the Auto Task Designer

## Configuration
Auto Tasks if enabled by an app on the Hornbill platform, will be accessible to configure via the admin console > Applications > [App] > Auto Tasks.
Auto Tasks can be configured against different entities in each different app. Ensure you choose the appropriate entity you wish to create the Auto Task workflow against from the drop down.
* Auto Tasks can be configured to be invoked from Custom Buttons on entity views in the different line of business applications.
* Auto Tasks will only be visible to invoke if the workflow is validated and marked as active.
* Auto Tasks will only be visible to invoke if the workflow is created for the relevant entity (see "Apps & Entities" section).

## Roles

|Name|Description|
|-|-|
|Workflow Manager|This role will enable a user to configure Auto Tasks against entities in an application from the admin console.|
|Form Designer|This role will enable a user to configure a custom button to invoke an Auto Task from a custom button on an entity view.|

Visibility of the custom buttons, from which an Auto Task workflow can be invoked is configurable per custom button on each entity view.

## Apps & Entities
Auto Tasks can be configured, and invoked via custom buttons on the following apps and entity views.

* Service Manager
* Requests
* Assets
* Document Manager
* Documents